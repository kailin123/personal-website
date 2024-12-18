---
authors:
- author-demo
categories:
- paige
- shortcodes
description: Demonstration of the code shortcode.
tags:
- code
- figures
title: Code
---

The `paige/code` shortcode displays code.

<!--more-->

## Basic

Code:

```go-html-template
{{</* paige/code */>}}
q = 'q = %r; print(q %% q)'; print(q % q)
{{</* /paige/code */>}}
```

Result:

{{< paige/code >}}
q = 'q = %r; print(q %% q)'; print(q % q)
{{< /paige/code >}}

---

Code:

```go-html-template
{{</* paige/code */>}}
                       ---
                    -        --
                --( /     \ )XXXXXXXXXXXXX
            --XXX(   O   O  )XXXXXXXXXXXXXXX-
           /XXX(       U     )        XXXXXXX\
         /XXXXX(              )--   XXXXXXXXXXX\
        /XXXXX/ (      O     )   XXXXXX   \XXXXX\
        XXXXX/   /            XXXXXX   \   \XXXXX----
        XXXXXX  /          XXXXXX         \  ----  -
---     XXX  /          XXXXXX      \           ---
  --  --  /      /\  XXXXXX            /     ---=
    -        /    XXXXXX              '--- XXXXXX
      --\/XXX\ XXXXXX                      /XXXXX
        \XXXXXXXXX                        /XXXXX/
         \XXXXXX                         /XXXXX/
           \XXXXX--  /                -- XXXX/
            --XXXXXXX---------------  XXXXX--
               \XXXXXXXXXXXXXXXXXXXXXXXX-
                 --XXXXXXXXXXXXXXXXXX-
{{</* /paige/code */>}}
```

Result:

{{< paige/code >}}
                       ---
                    -        --
                --( /     \ )XXXXXXXXXXXXX
            --XXX(   O   O  )XXXXXXXXXXXXXXX-
           /XXX(       U     )        XXXXXXX\
         /XXXXX(              )--   XXXXXXXXXXX\
        /XXXXX/ (      O     )   XXXXXX   \XXXXX\
        XXXXX/   /            XXXXXX   \   \XXXXX----
        XXXXXX  /          XXXXXX         \  ----  -
---     XXX  /          XXXXXX      \           ---
  --  --  /      /\  XXXXXX            /     ---=
    -        /    XXXXXX              '--- XXXXXX
      --\/XXX\ XXXXXX                      /XXXXX
        \XXXXXXXXX                        /XXXXX/
         \XXXXXX                         /XXXXX/
           \XXXXX--  /                -- XXXX/
            --XXXXXXX---------------  XXXXX--
               \XXXXXXXXXXXXXXXXXXXXXXXX-
                 --XXXXXXXXXXXXXXXXXX-
{{< /paige/code >}}

## Lang parameter

Code:

```go-html-template
{{</* paige/code lang="c" */>}}
float Q_rsqrt( float number )
{
	long i;
	float x2, y;
	const float threehalfs = 1.5F;

	x2 = number * 0.5F;
	y  = number;
	i  = * ( long * ) &y;
	i  = 0x5f3759df - ( i >> 1 );
	y  = * ( float * ) &i;
	y  = y * ( threehalfs - ( x2 * y * y ) );

	return y;
}
{{</* /paige/code */>}}
```

Result:

{{< paige/code lang="c" >}}
float Q_rsqrt( float number )
{
	long i;
	float x2, y;
	const float threehalfs = 1.5F;

	x2 = number * 0.5F;
	y  = number;
	i  = * ( long * ) &y;
	i  = 0x5f3759df - ( i >> 1 );
	y  = * ( float * ) &i;
	y  = y * ( threehalfs - ( x2 * y * y ) );

	return y;
}
{{< /paige/code >}}


## Options parameter

Code:

```go-html-template
{{</* paige/code options="linenos=true,hl_lines=10" */>}}
float Q_rsqrt( float number )
{
	long i;
	float x2, y;
	const float threehalfs = 1.5F;

	x2 = number * 0.5F;
	y  = number;
	i  = * ( long * ) &y;
	i  = 0x5f3759df - ( i >> 1 );
	y  = * ( float * ) &i;
	y  = y * ( threehalfs - ( x2 * y * y ) );

	return y;
}
{{</* /paige/code */>}}
```

Result:

{{< paige/code options="linenos=true,hl_lines=10" >}}
float Q_rsqrt( float number )
{
	long i;
	float x2, y;
	const float threehalfs = 1.5F;

	x2 = number * 0.5F;
	y  = number;
	i  = * ( long * ) &y;
	i  = 0x5f3759df - ( i >> 1 );
	y  = * ( float * ) &i;
	y  = y * ( threehalfs - ( x2 * y * y ) );

	return y;
}
{{< /paige/code >}}

## Unescape parameter

Code:

```go-html-template
{{</* paige/code unescape=false */>}}
{{</* paige/request "[...]" */>}}
{{</* /paige/code */>}}
```

Result:

{{< paige/code unescape=false >}}
{{< paige/request "https://gist.githubusercontent.com/willfaught/fe6f6a8b9715e70112b6894935ecbecd/raw/64f41b7eb47ed5a60172217f8ba3868c23f69d21/qrsqrt.c" >}}
{{< /paige/code >}}

---

Code:

```go-html-template
{{</* paige/code unescape=true */>}}
{{</* paige/request "[...]" */>}}
{{</* /paige/code */>}}
```

Result:

{{< paige/code unescape=true >}}
{{< paige/request "https://gist.githubusercontent.com/willfaught/fe6f6a8b9715e70112b6894935ecbecd/raw/64f41b7eb47ed5a60172217f8ba3868c23f69d21/qrsqrt.c" >}}
{{< /paige/code >}}

## Figure

Code:

```go-html-template
{{</* paige/figure caption="Quine" */>}}
{{</* paige/code lang="python" */>}}
q = 'q = %r; print(q %% q)'; print(q % q)
{{</* /paige/code */>}}
{{</* /paige/figure */>}}
```

Result:

{{< paige/figure caption="Quine" >}}
{{< paige/code lang="python" >}}
q = 'q = %r; print(q %% q)'; print(q % q)
{{< /paige/code >}}
{{< /paige/figure >}}
