---
UID: NF:directxmath.XMComparisonAnyFalse
title: XMComparisonAnyFalse function (directxmath.h)
description: Tests the comparison value to determine if any of the compared components are false.
helpviewer_keywords: ["Use DirectX..XMComparisonAnyFalse","XMComparisonAnyFalse","XMComparisonAnyFalse method [DirectX Math Support APIs]","dxmath.xmcomparisonanyfalse"]
old-location: dxmath\xmcomparisonanyfalse.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMComparisonAnyFalse(uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMComparisonAnyFalse, XMComparisonAnyFalse, XMComparisonAnyFalse method [DirectX Math Support APIs], dxmath.xmcomparisonanyfalse
req.header: directxmath.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: Use DirectX.
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XMComparisonAnyFalse
 - directxmath/XMComparisonAnyFalse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMComparisonAnyFalse
---

# XMComparisonAnyFalse function


## -description

Tests the comparison value to determine if any of the compared components are false.

## -parameters

### -param CR [in]

Comparison value to test. The comparison value is typically retrieved using a recording version of a DirectXMath
        function such as <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4equalr">XMVector4EqualR</a>. The names of the recording functions
        end with an "R".

## -returns

Returns true if any of the compared components are false.

## -remarks

The following code snippet highlights how this function might be used:


```
uint32_t comparisonValue = XMVector4EqualR( V1, V2 );
if( XMComparisonAnyFalse( comparisonValue ) )
{
	DoStuff();
}
```


The <code>DoStuff</code> function will be called only if any of the four components of <i>V1</i> and <i>V2</i> are
   different (any of the compared components are false).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-utilities">DirectXMath Library Utility Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmcomparisonallfalse">XMComparisonAllFalse</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmcomparisonallinbounds">XMComparisonAllInBounds</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmcomparisonalltrue">XMComparisonAllTrue</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmcomparisonanyoutofbounds">XMComparisonAnyOutOfBounds</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmcomparisonanytrue">XMComparisonAnyTrue</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmcomparisonmixed">XMComparisonMixed</a>