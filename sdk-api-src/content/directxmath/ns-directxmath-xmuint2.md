---
UID: NS:directxmath.XMUINT2
title: XMUINT2
author: windows-sdk-content
description: A 2D vector where each component is an unsigned integer.
old-location: dxmath\xmuint2.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUINT2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: XMUINT2, XMUINT2 structure [DirectX Math Support APIs], directxmath/XMUINT2, dxmath.xmuint2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectXMath.h
api_name:
 - XMUINT2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMUINT2 structure


## -description


A 2D vector where each component is an unsigned integer.

For a list of additional functionality such as constructors and operators that are available using <code>XMUINT2</code> when you
  are programming in C++, see <a href="https://msdn.microsoft.com/563e5026-1746-483b-80b0-fb931bcf057a">XMUINT2 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type Equivalences</a> for information about
  equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and
  <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields




### -field x

Unsigned integer value describing the x-coordinate of the vector.


### -field y

Unsigned integer value describing the y-coordinate of the vector.


## -remarks



You can use <a href="https://msdn.microsoft.com/2dc3964f-9c5f-44c6-ae3f-6cc79e8f5470">XMLoadUInt2</a> to load <code>XMUINT2</code> into instances 
   of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.

You can use <a href="https://msdn.microsoft.com/69460147-3abe-4412-bbf2-184e60c65534">XMStoreUInt2</a> to store instances of <code>XMVECTOR</code> 
     into an instance of <code>XMUINT2</code>.

<b>Namespace:</b> Use DirectX

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/563e5026-1746-483b-80b0-fb931bcf057a">XMUINT2 Extensions</a>
 

 

