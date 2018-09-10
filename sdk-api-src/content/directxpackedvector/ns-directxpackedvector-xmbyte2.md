---
UID: NS:directxpackedvector.XMBYTE2
title: XMBYTE2
author: windows-sdk-content
description: A 2D vector where each component is a signed integer, 8-bits (1 byte) in length.
old-location: dxmath\xmbyte2.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMBYTE2
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: XMBYTE2, XMBYTE2 structure [DirectX Math Support APIs], XMBYTE2 structure,about XMBYTE2 structure, directxpackedvector/XMBYTE2, dxmath.xmbyte2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: directxpackedvector.h
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
 - DirectXPackedVector.h
api_name:
 - XMBYTE2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMBYTE2 structure


## -description


A 2D vector where each component is a signed integer, 8-bits (1 byte) in length.

For a list of additional functionality such as constructors and operators that are available using <code>XMBYTE2</code> when you
  are programming in C++, see <a href="https://msdn.microsoft.com/4b01065e-28de-4c67-92ed-2a3564817656">XMBYTE2 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type Equivalences</a> for information about
  equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and
  <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields




### -field x

Signed 8-bit integer value in the range [-127, 127] describing the x-coordinate of the vector.


### -field y

Signed 8-bit integer value in the range [-127, 127] describing the y-coordinate of the vector.


### -field v

 




## -remarks



You can use <a href="https://msdn.microsoft.com/daaa44b6-92a8-4847-9443-fc976b8a2011">XMLoadByte2</a> to load <code>XMBYTE2</code> into instances 
   of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.

You can use <a href="https://msdn.microsoft.com/279921ec-eaa5-46c8-af5d-ea4b9ade72a0">XMStoreByte2</a> to store instances of <code>XMVECTOR</code> 
     into an instance of <code>XMBYTE2</code>.

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/4b01065e-28de-4c67-92ed-2a3564817656">XMBYTE2 Extensions</a>
 

 

