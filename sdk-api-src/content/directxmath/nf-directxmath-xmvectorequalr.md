---
UID: NF:directxmath.XMVectorEqualR
title: XMVectorEqualR function
author: windows-sdk-content
description: Performs a per-component test for equality of two vectors and sets a comparison value that can be examined using functions such as XMComparisonAllTrue.
old-location: dxmath\xmvectorequalr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.comparison.XMVectorEqualR(uint32_t@,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMVectorEqualR, XMVectorEqualR, XMVectorEqualR method [DirectX Math Support APIs], dxmath.xmvectorequalr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxmath.h
req.include-header: DirectXMath.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxmathvector.inl
api_name:
 - XMVectorEqualR
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVectorEqualR
: 
---

# XMVectorEqualR function


## -description


Performs a per-component test for equality of two vectors and sets a comparison value that can be examined using functions such as <a href="https://msdn.microsoft.com/74d2856d-c311-47cd-9ff0-ee10ed66e29e">XMComparisonAllTrue</a>.


## -parameters




### -param pCR [out]

Pointer to a <b>uint32_t</b> comparison value that can be examined using functions such as <a href="https://msdn.microsoft.com/74d2856d-c311-47cd-9ff0-ee10ed66e29e">XMComparisonAllTrue</a>. The <code>XMComparisonXXXX</code> functions may be used to further test the number of components that passed the comparison.


### -param V1 [in]

First vector to compare.


### -param V2 [in]

Second vector to compare.


## -returns



Returns a vector containing the results of each component test.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/8caad40f-ab8e-db2f-da11-18f3d3ccf6ef">Vector Comparison Functions</a>



<a href="https://msdn.microsoft.com/e5e3d343-6baf-4d98-b303-5d1b12bb285d">XMVectorEqual</a>



<a href="https://msdn.microsoft.com/f96b619f-8aa2-47ab-8a3b-48000b9008bb">XMVectorEqualInt</a>
 

 

