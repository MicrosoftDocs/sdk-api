---
UID: NS:directxmath.XMINT4
title: XMINT4
author: windows-sdk-content
description: A 4D vector where each component is a signed integer.
old-location: dxmath\xmint4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMINT4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMINT4, XMINT4 structure [DirectX Math Support APIs], directxmath/XMINT4, dxmath.xmint4
ms.prod: windows
ms.technology: windows-sdk
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
 - XMINT4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMINT4 structure


## -description


A 4D vector where each component is a signed integer.

For a list of more functionality such as constructors and operators that are available 
  using <code>XMINT4</code> when you
  are programming in C++, see <a href="https://msdn.microsoft.com/bbe13052-f07d-488f-b643-535195d4e9ea">XMINT4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type Equivalences</a> for information about
  equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and
  <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields




### -field x

Signed integer value describing the x coordinate of the vector.


### -field y

Signed integer value describing the y coordinate of the vector.


### -field z

Signed integer value describing the z coordinate of the vector.


### -field w

Signed integer value describing the w coordinate of the vector.


## -remarks



You can use <a href="https://msdn.microsoft.com/b68ec578-1196-42b4-853b-1fd6e70798d2">XMLoadSInt4</a> to load <code>XMINT4</code> into instances 
   of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.

You can use <a href="https://msdn.microsoft.com/ca914f14-289c-4332-8edf-8e385f4a5a9d">XMStoreSInt4</a> to store instances of <code>XMVECTOR</code> 
     into an instance of <code>XMINT4</code>.

<b>Namespace:</b> Use DirectX

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/bbe13052-f07d-488f-b643-535195d4e9ea">XMINT4 Extensions</a>
 

 

