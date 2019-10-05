---
UID: NS:directxmath.XMFLOAT3A
title: XMFLOAT3A
description: Describes an XMFLOAT3 structure aligned on a 16-byte boundary.
ms.assetid: bad51162-3eaa-44e1-9032-6db3e75f0e99
ms.author: windowssdkdev
ms.date: 05/20/2019
ms.keywords: XMFLOAT3A
ms.topic: language-reference
f1_keywords: 
 - "directxmath/XMFLOAT3A"
dev_langs:
 - c++
targetos: Windows
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
 - XMFLOAT3A
---

# XMFLOAT3A structure

## -description

Describes an <a href="https://msdn.microsoft.com/115a901e-ca61-4895-b93f-09b53dbc313f">XMFLOAT3</a> structure aligned on a 16-byte boundary.

<div class="alert"><b>Note</b>  See <a href="https://docs.microsoft.com/windows/desktop/dxmath/pg-xnamath-internals">DirectXMath Library Type Equivalences</a> for information
  about equivalent <a href="https://msdn.microsoft.com/993fc7e4-4752-4bce-82d0-0a034fdc69c0">D3DDECLTYPE</a>, <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>, and
  <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> objects.</div>

## -struct-fields

### -field XMFLOAT3

An **XMFLOAT3** object.

## -remarks

<code>XMFLOAT3A</code> can be loaded into instances of <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> by using <a href="https://msdn.microsoft.com/009681d9-8e9b-4436-bd76-0c38c9035d10">XMLoadFloat3A</a>.

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT3A</code> with <a href="https://msdn.microsoft.com/47ee9908-29df-41bf-8a1a-515d20b21d88">XMStoreFloat3A</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>

<a href="https://msdn.microsoft.com/115a901e-ca61-4895-b93f-09b53dbc313f">XMFLOAT3</a>
