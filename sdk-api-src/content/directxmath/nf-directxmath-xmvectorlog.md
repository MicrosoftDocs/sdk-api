---
UID: NF:directxmath.XMVectorLog
title: XMVectorLog function
author: windows-sdk-content
description: Computes the base two logarithm of each component of a vector.Note  This function is a compatibility alias for XMVectorLog2 for existing Windows 8 code.
old-location: dxmath\xmvectorlog.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transcendental.XMVectorLog(XMVECTOR)
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Use DirectX..XMVectorLog, XMVectorLog, XMVectorLog method [DirectX Math Support APIs], dxmath.xmvectorlog
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
 - XMVectorLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorLog function


## -description


Computes the base two logarithm of each component of a vector.<div class="alert"><b>Note</b>  This function is a compatibility alias for <a href="https://msdn.microsoft.com/92C911B4-5BC7-443D-BCBB-F4838E24E607">XMVectorLog2</a> for existing Windows 8 code. This function is deprecated for Windows 8.1. Don't use it and instead use <b>XMVectorLog2</b> or <a href="https://msdn.microsoft.com/C092B786-BAB8-4F8F-95D2-3C23F59EF064">XMVectorLogE</a>.
</div>
<div> </div>



## -parameters




### -param V [in]

Vector for which to compute the base two logarithm.


## -returns



Returns a vector whose components are base two logarithm of the corresponding components of <i>V</i>.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/aae12d4a-7758-83df-5376-99d5d94a28c4">Transcendental Vector Functions</a>
 

 

