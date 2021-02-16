---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateResourceTexture
title: ID2D1EffectContext::CreateResourceTexture (d2d1effectauthor.h)
description: Creates or finds the given resource texture, depending on whether a resource id is specified.
helpviewer_keywords: ["CreateResourceTexture","CreateResourceTexture method [Direct2D]","CreateResourceTexture method [Direct2D]","ID2D1EffectContext interface","ID2D1EffectContext interface [Direct2D]","CreateResourceTexture method","ID2D1EffectContext.CreateResourceTexture","ID2D1EffectContext::CreateResourceTexture","d2d1effectauthor/ID2D1EffectContext::CreateResourceTexture","direct2d.id2d1contextinternal_createresourcetexture"]
old-location: direct2d\id2d1contextinternal_createresourcetexture.htm
tech.root: Direct2D
ms.assetid: 265888DA-03C2-42F0-92D8-FEB542F9BAA4
ms.date: 12/05/2018
ms.keywords: CreateResourceTexture, CreateResourceTexture method [Direct2D], CreateResourceTexture method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateResourceTexture method, ID2D1EffectContext.CreateResourceTexture, ID2D1EffectContext::CreateResourceTexture, d2d1effectauthor/ID2D1EffectContext::CreateResourceTexture, direct2d.id2d1contextinternal_createresourcetexture
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2D1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1EffectContext::CreateResourceTexture
 - d2d1effectauthor/ID2D1EffectContext::CreateResourceTexture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext.CreateResourceTexture
---

# ID2D1EffectContext::CreateResourceTexture


## -description

Creates or finds the given resource texture, depending on whether a resource id is specified. It also optionally initializes the texture with the specified data.

## -parameters

### -param resourceId [in, optional]

Type: <b>const GUID*</b>

An optional pointer to the unique id that identifies the lookup table.

### -param resourceTextureProperties [in]

Type: <b>const <a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_resource_texture_properties">D2D1_RESOURCE_TEXTURE_PROPERTIES</a>*</b>

The properties used to create the resource texture.

### -param data [in, optional]

Type: <b>const BYTE*</b>

The optional data to be loaded into the resource texture.

### -param strides [in, optional]

Type: <b>const UINT32*</b>

An optional pointer to the stride to advance through the resource texture, according to dimension.

### -param dataSize

Type: <b>UINT32</b>

The size, in bytes, of the data.

### -param resourceTexture [out]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1resourcetexture">ID2D1ResourceTexture</a>**</b>

The returned texture that can be used as a resource in a Direct2D effect.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext">ID2D1EffectContext</a>