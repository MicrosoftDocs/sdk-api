---
UID: NS:directxpackedvector.XMUBYTE2
title: XMUBYTE2
author: windows-driver-content
description: Describes a 2D vector where each component is a unsigned integer, 8-bits (1 byte) in length.
old-location: dxmath\xmubyte2.htm
old-project: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMUBYTE2
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: XMUBYTE2, XMUBYTE2 structure [DirectX Math Support APIs], _XMUBYTE2, _XMUBYTE2 structure [DirectX Math Support APIs], directxpackedvector/XMUBYTE2, dxmath.xmubyte2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.namespace: DirectX::PackedVector
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	DirectXPackedVector.h
api_name:
-	_XMUBYTE2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMUBYTE2 structure


## -description


Describes a 2D vector where each component is a unsigned integer, 8-bits (1 byte) in length.

A 2D vector where each component is a unsigned integer, 8-bits (1 byte) in length.



For a list of additional functionality such as constructors and operators that are available using <code>XMUBYTE2</code> when you
  are programming in C++, see <a href="https://msdn.microsoft.com/552af402-2995-4b07-b982-83be27caa017">XMUBYTE2 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type Equivalences</a> for information about
  equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and
  <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields




### -field x

Unsigned 8-bit integer value in the range [0, 255] describing the x-coordinate of the vector.


### -field y

Unsigned 8-bit integer value in the range [0, 255] describing the y-coordinate of the vector.


## -remarks




     You can use <a href="https://msdn.microsoft.com/fee3467c-8805-463e-9928-67a9d08c4f33">XMLoadUByte2</a> to load <code>XMUBYTE2</code> 
     into instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.

You can use <a href="https://msdn.microsoft.com/8dc12889-34b2-4c56-95e7-d2f0592e3299">XMStoreUByte2</a> to store instances of <code>XMVECTOR</code> 
   into an instance of <code>XMUBYTE2</code>.

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/552af402-2995-4b07-b982-83be27caa017">XMUBYTE2 Extensions</a>
 

 

