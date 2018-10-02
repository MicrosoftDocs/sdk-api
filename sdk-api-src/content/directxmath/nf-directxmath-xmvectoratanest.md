---
UID: NF:directxmath.XMVectorATanEst
title: XMVectorATanEst function
author: windows-sdk-content
description: Estimates the arctangent of each component of an XMVECTOR.
old-location: dxmath\xmvectoratanest.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transcendental.XMVectorATanEst(XMVECTOR)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVectorATanEst, XMVectorATanEst, XMVectorATanEst method [DirectX Math Support APIs], dxmath.xmvectoratanest
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
 - XMVectorATanEst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorATanEst function


## -description


Estimates the arctangent of each component of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param V [in]

Vector for which to compute the arctangent.


## -returns



Returns a vector whose components are estimates of the arctangent of the corresponding components of <i>V</i>.




## -remarks



<code>Est</code> functions offer increased performance at the expense of reduced accuracy.
    <code>Est</code> functions are appropriate for non-critical calculations where accuracy can be sacrificed for speed.
    The exact amount of lost accuracy and speed increase are platform dependent.

This function uses a 9-degree minimax approximation.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/aae12d4a-7758-83df-5376-99d5d94a28c4">Transcendental Vector Functions</a>



<a href="https://msdn.microsoft.com/b7fe0cd6-a447-4123-8715-8f540fdcced6">XMVectorATan</a>



<a href="https://msdn.microsoft.com/f39d7f8e-49a8-428e-b115-e91a9412d13c">XMVectorATan2</a>



<a href="https://msdn.microsoft.com/74bbff16-011f-46b4-b97c-8ca620267014">XMVectorATan2Est</a>



<a href="https://msdn.microsoft.com/6555d1a8-fb83-4e29-877f-3efb845eb620">XMVectorTan</a>
 

 

