---
UID: NS:directxmath.XMFLOAT4X4
title: XMFLOAT4X4 (directxmath.h)
author: windows-sdk-content
description: A 4*4 floating point matrix.
old-location: dxmath\xmfloat4x4.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMFLOAT4X4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: XMFLOAT4X4, XMFLOAT4X4 structure [DirectX Math Support APIs], directxmath/XMFLOAT4X4, dxmath.xmfloat4x4
ms.topic: struct
f1_keywords: ["directxmath/XMFLOAT4X4"]
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
 - XMFLOAT4X4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMFLOAT4X4 structure


## -description


A 4*4 floating point matrix.



For a list of additional functionality such as constructors and operators that are available using <code>XMFLOAT4X4</code> when you
  are programming in C++, see <a href="https://msdn.microsoft.com/ae6a5159-4a77-488c-a836-da3a16e7fcaf">XMFLOAT4X4 Extensions</a>.
<div class="alert"><b>Note</b>  See <a href="https://docs.microsoft.com/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type Equivalences</a> for information about
  equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and
  <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.</div><div> </div>

## -struct-fields




### -field _11

An element of the matrix.


### -field _12

An element of the matrix.


### -field _13

An element of the matrix.


### -field _14

An element of the matrix.


### -field _21

An element of the matrix.


### -field _22

An element of the matrix.


### -field _23

An element of the matrix.


### -field _24

An element of the matrix.


### -field _31

An element of the matrix.


### -field _32

An element of the matrix.


### -field _33

An element of the matrix.


### -field _34

An element of the matrix.


### -field _41

An element of the matrix.


### -field _42

An element of the matrix.


### -field _43

An element of the matrix.


### -field _44

An element of the matrix.


### -field m

A 4*4 array representing the matrix.


### -field operator=

TBD 


### -field XMFLOAT4X4

TBD 


### -field operator()

TBD 




## -remarks



Scalar members of <code>XMFLOAT4X4</code> are of the form <b>_</b><i>RowCol</i>, and provide one based indexing,
   where <i>Row</i> specifies the one's based matrix row (running from 1 to 4), and
   <i>Col</i> specifies the one's based matrix column (running from 1 to 4).

The two dimensional 4*4 array member of <code>XMFLOAT4X4</code>, <b>m</b>, provides zero based indexing of the structure's
   matrix. When accessing <code>XMFLOAT4X4</code><b>m[</b><i>Row</i><b>,</b><i>Col</i><b>]</b>, <i>Row</i> can run from 0 to 3 and <i>Col</i> can run from 0 to 3.

<code>XMFLOAT4X4</code> can be loaded into instances of <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type"> XMVECTOR</a> by using
   <a href="https://msdn.microsoft.com/51c2a4e8-99c9-4a3d-8fe4-06b534693146">XMLoadFloat4x4</a>.

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT4X4</code> with
   <a href="https://msdn.microsoft.com/8d569b41-a22c-419e-a50a-eaab20a6a8a2">XMStoreFloat4x4</a>.

<b>Namespace:</b> Use DirectX

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="https://msdn.microsoft.com/ae6a5159-4a77-488c-a836-da3a16e7fcaf">XMFLOAT4X4 Extensions</a>



<a href="https://msdn.microsoft.com/64dd4128-103b-4d54-98f3-cc908170d81c">XMMATRIX</a>
 

 

