# javascript-type-evaluations
Simple javascript program to evaluate and print various expressions

```
       expr or value       eval   typeof()   Number()  isNaN()  Boolean()    in an object
-------------------------------------------------------------------------------------------------
            00000000          0     number          0    false      false    {"thing":0}
          "00000000"   00000000     string          0    false       true    {"thing":"00000000"}
          0x00000000          0     number          0    false      false    {"thing":0}
            A29FC801   A29FC801     string        NaN     true       true    {"thing":"A29FC801"}
          0xA29FC801 2728380417     number 2728380417    false       true    {"thing":2728380417}
                 101        101     number        101    false       true    {"thing":101}
                1.01       1.01     number       1.01    false       true    {"thing":1.01}
                 1e6    1000000     number    1000000    false       true    {"thing":1000000}
                 1/0   Infinity     number   Infinity    false       true    {"thing":null}
                 0/0        NaN     number        NaN     true      false    {"thing":null}
                  ""                string          0    false      false    {"thing":""}
                 "0"          0     string          0    false       true    {"thing":"0"}
               "1.1"        1.1     string        1.1    false       true    {"thing":"1.1"}
                   0          0     number          0    false      false    {"thing":0}
                  -0          0     number          0    false      false    {"thing":0}
                null       null     object          0    false      false    {"thing":null}
           undefined  undefined  undefined        NaN     true      false    {}
   undefined == null       true    boolean          1    false       true    {"thing":true}
          !undefined       true    boolean          1    false       true    {"thing":true}
       undefined - 1        NaN     number        NaN     true      false    {"thing":null}
       undefined * 1        NaN     number        NaN     true      false    {"thing":null}
       undefined / 0        NaN     number        NaN     true      false    {"thing":null}
       undefined > 0      false    boolean          0    false      false    {"thing":false}
       undefined > 1      false    boolean          0    false      false    {"thing":false}
       undefined < 1      false    boolean          0    false      false    {"thing":false}
      undefined == 0      false    boolean          0    false      false    {"thing":false}
      undefined != 0       true    boolean          1    false       true    {"thing":true}
       1 > undefined      false    boolean          0    false      false    {"thing":false}
          -undefined        NaN     number        NaN     true      false    {"thing":null}
    undefined || NaN        NaN     number        NaN     true      false    {"thing":null}
   undefined || null       null     object          0    false      false    {"thing":null}
   undefined == null       true    boolean          1    false       true    {"thing":true}
    undefined == NaN      false    boolean          0    false      false    {"thing":false}
         [undefined]                object          0    false       true    {"thing":[null]}
 [undefined].shift()  undefined  undefined        NaN     true      false    {}
      [null].shift()       null     object          0    false      false    {"thing":null}
               "foo"        foo     string        NaN     true       true    {"thing":"foo"}
            Infinity   Infinity     number   Infinity    false       true    {"thing":null}
           -Infinity  -Infinity     number  -Infinity    false       true    {"thing":null}
 Infinity / Infinity        NaN     number        NaN     true      false    {"thing":null}
 Infinity - Infinity        NaN     number        NaN     true      false    {"thing":null}
        Infinity / 2   Infinity     number   Infinity    false       true    {"thing":null}
 Infinity * Infinity   Infinity     number   Infinity    false       true    {"thing":null}
        Infinity * 0        NaN     number        NaN     true      false    {"thing":null}
        Infinity * 1   Infinity     number   Infinity    false       true    {"thing":null}
        Infinity + 1   Infinity     number   Infinity    false       true    {"thing":null}
      Infinity - 1e9   Infinity     number   Infinity    false       true    {"thing":null}
                 NaN        NaN     number        NaN     true      false    {"thing":null}
           NaN + NaN        NaN     number        NaN     true      false    {"thing":null}
          NaN == NaN      false    boolean          0    false      false    {"thing":false}
         NaN === NaN      false    boolean          0    false      false    {"thing":false}
    isNaN(undefined)       true    boolean          1    false       true    {"thing":true}
     isNaN(Infinity)      false    boolean          0    false      false    {"thing":false}
         isNaN(null)      false    boolean          0    false      false    {"thing":false}
         isNaN(true)      false    boolean          0    false      false    {"thing":false}
        isNaN(false)      false    boolean          0    false      false    {"thing":false}
       isNaN("junk")       true    boolean          1    false       true    {"thing":true}
                true       true    boolean          1    false       true    {"thing":true}
               false      false    boolean          0    false      false    {"thing":false}
              "true"       true     string        NaN     true       true    {"thing":"true"}
             "false"      false     string        NaN     true       true    {"thing":"false"}
               "str"        str     string        NaN     true       true    {"thing":"str"}
   typeof(typeof(1))     string     string        NaN     true       true    {"thing":"string"}
```
