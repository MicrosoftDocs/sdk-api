---
UID: NS:directxmath.XMINT3
title: XMINT3 (directxmath.h)
author: windows-sdk-content
description: A 3D vector where each component is a signed integer.
old-location: dxmath\xmint3.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMINT3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMINT3, XMINT3 structure [DirectX Math Support APIs], directxmath/XMINT3, dxmath.xmint3
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
 - XMINT3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMINT3 structure


## -description


A 3D vector where each component is a signed integer.

For a list of more functionality such as constructors and operators that are available using <code>XMINT3</code> when you
  are programming in C++, see <a href="https://msdn.microsoft.com/en-us/library/Hh449512(v=VS.85).aspx">XMINT3 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type Equivalences</a> for information about
  equivalent <a href="https://msdn.microsoft.com/en-us/library/Bb172533(v=VS.85).aspx">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a>, and
  <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields




### -field x

Signed integer value describing the x coordinate of the vector.


### -field y

Signed integer value describing the y coordinate of the vector.


### -field z

Signed integer value describing the z coordinate of the vector.


### -field operator=

TBD 


### -field XMINT3

TBD 




## -remarks



You can use <a href="https://msdn.microsoft.com/en-us/library/Hh404676(v=VS.85).aspx">XMLoadSInt3</a> to load <code>XMINT3</code> into instances 
   of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.

You can use <a href="https://msdn.microsoft.com/en-us/library/Hh404702(v=VS.85).aspx">XMStoreSInt3</a> to store instances of <code>XMVECTOR</code> 
     into an instance of <code>XMINT3</code>.

<b>Namespace:</b> Use DirectX

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449512(v=VS.85).aspx">XMINT3 Extensions</a>
 

 

