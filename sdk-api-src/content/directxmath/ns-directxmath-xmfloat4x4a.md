---
UID: NS:directxmath.XMFLOAT4X4A
title: XMFLOAT4X4A
description: Describes an XMFLOAT4X4 structure aligned on a 16-byte boundary.
ms.assetid: 30563f47-6990-4d94-a587-5c64a389762f
ms.author: windowssdkdev
ms.date: 05/20/2019
ms.keywords: XMFLOAT4X4A
ms.topic: language-reference
targetos: Windows
product: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: directxmath.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - directxmath.h
api_name:
 - XMFLOAT4X4A
---

# XMFLOAT4X4A Structure

## -description

Describes an <a href="https://msdn.microsoft.com/en-us/library/Ee419621(v=VS.85).aspx">XMFLOAT4X4</a> structure aligned on a 16-byte boundary.

<div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/31512657-c413-9e6e-e343-1ea677a02b8c">DirectXMath Library Type Equivalences</a> for information about equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.</div>

## -struct-fields

### -field XMFLOAT4X4

An **XMFLOAT4X4** object.

## -remarks

<code>XMFLOAT4X4A</code> can be loaded into instances of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> by using **XMLoadFloat4x4A**.

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT4X4A</code> with **XMStoreFloat4x4A**.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3> Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="https://msdn.microsoft.com/58acb05d-e79b-8f42-4cf4-76ae57929739">DirectXMath Library Structures</a>

<a href="https://msdn.microsoft.com/en-us/library/Ee419621(v=VS.85).aspx">XMFLOAT4X4</a>
