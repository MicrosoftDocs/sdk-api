---
UID: NS:directxmath.XMMATRIX
title: XMMATRIX
author: windows-sdk-content
description: Describes a 4*4 matrix aligned on a 16-byte boundary that maps to four hardware vector registers.
old-location: dxmath\xmmatrix.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMMATRIX
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMMATRIX, XMMATRIX structure [DirectX Math Support APIs], directxmath/XMMATRIX, dxmath.xmmatrix
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
 - XMMATRIX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMMATRIX structure


## -description


Describes a 4*4 matrix aligned on a 16-byte boundary that maps to four hardware vector registers.

DirectXMath uses row-major matrices, row vectors, and pre-multiplication. Handedness is determined by which function version is used (RH vs. LH).

For a list of additional functionality such as constructors and operators that are available using <code>XMMATRIX</code> when you
  are programming in C++, see <a href="https://msdn.microsoft.com/651d17f4-7af6-4f20-91ec-903c3602e4b2">XMMATRIX Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type Equivalences</a> for information about
  equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and
  <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields




### -field _11

 


### -field _12

 


### -field _13

 


### -field _14

 


### -field _21

 


### -field _22

 


### -field _23

 


### -field _24

 


### -field _31

 


### -field _32

 


### -field _33

 


### -field _34

 


### -field _41

 


### -field _42

 


### -field _43

 


### -field _44

 


### -field m

 


### -field r

Array of four vectors, representing the rows of the matrix.


## -remarks



In the DirectXMath.h header file, the system uses an alias to the <code>XMMATRIX</code> object, specifically <b>CXMMATRIX</b>.
   The header uses the alias to comply with the optimal in-line calling conventions of different compilers. For most
   projects using DirectXMath it is sufficient to simply treat this as an exact alias to <code>XMMATRIX</code>.

Effectively:


```

typedef const XMMATRIX CXMMATRIX;

```


For projects that need detailed information about how different platform's calling conventions are handled, see
   <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">Library Internals</a>.

<code>XMMATRIX</code> is row-major and all DirectXMath functions that accept an <code>XMMATRIX</code> as a parameter expect data to be organized as row-major.

Data in an <code>XMMATRIX</code> has the following layout.


```

_11 _12 _13 _14
_21 _22 _23 _24
_31 _32 _33 _34
_41 _42 _43 _44

```


DirectXMath defines <b>XMMATRIX</b> as a fully opaque type. To access individual elements of <b>XMMATRIX</b>, use equivalent types such as <a href="https://msdn.microsoft.com/2af4929b-9e44-4229-916e-d7d8eae07306">XMFLOAT4</a> for a given row or <a href="https://msdn.microsoft.com/92991b18-60a5-41ec-85de-690ac6e5f1e2">XMFLOAT4X4</a> for the whole matrix.

<div class="alert"><b>Note</b>  XNAMath 2.x defines <code>XMMATRIX</code> as a union with <b>_11</b> to <b>_44</b> members and an <b>m</b> array member. When you use these members of the union, poor performance results. DirectXMath.h still defines these <code>XMMATRIX</code> union members for when you build an app with <a href="https://msdn.microsoft.com/c1746b7b-7e7e-2453-77eb-17f859a38fe2">_XM_NO_INTRINSICS_</a>. XNAMath version 2.05 provides an opt-in XM_STRICT_XMMATRIX to enforce the DirectXMath behavior.</div>
<div> </div>
<b>Namespace:</b> Use DirectX

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/92991b18-60a5-41ec-85de-690ac6e5f1e2">XMFLOAT4X4</a>



<a href="https://msdn.microsoft.com/651d17f4-7af6-4f20-91ec-903c3602e4b2">XMMATRIX Extensions</a>
 

 

