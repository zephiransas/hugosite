---
title: "Second Post"
date: 2017-09-08T10:07:19+09:00
draft: false
---

それでは実際のテストを書いて行きましょう。ここでのテストシナリオは

- includeTaxメソッドに100を渡した場合に、108が返ってくること

をテストするとします。これをlambda-behaveで書くと、以下のようになります。

``` java
import static com.insightfullogic.lambdabehave.Suite.*;

@RunWith(JunitSuiteRunner.class)
public class SampleSpec {{
    describe("includeTax", it -> {
        it.should("税込み価格が取得できること", expect ->
            expect.that(Sample.includeTax(100)).is(108)
        );
    });
}}
```
