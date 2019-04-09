---
UID: NF:directxmath.XMVector2LengthEst
title: XMVector2LengthEst function (directxmath.h)
author: windows-sdk-content
description: Estimates the length of a 2D vector.
old-location: dxmath\xmvector2lengthest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector2LengthEst(XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector2LengthEst, XMVector2LengthEst, XMVector2LengthEst method [DirectX Math Support APIs], dxmath.xmvector2lengthest
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
 - XMVector2LengthEst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVector2LengthEst function


## -description


Estimates the length of a 2D vector.


## -parameters




### -param V [in]

2D vector.


## -returns



Returns a vector, each of whose components are estimates of the length of <i>V</i>.




## -remarks



<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/a17cdad7-4fbe-bf83-472f-1b99603b7fec">DirectXMath Library 2D Vector Geometric Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee420775(v=VS.85).aspx">XMVector2Length</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee420778(v=VS.85).aspx">XMVector2LengthSq</a>
 

 

