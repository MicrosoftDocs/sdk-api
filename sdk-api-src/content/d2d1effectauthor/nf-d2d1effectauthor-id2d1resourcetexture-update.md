---
UID: NF:d2d1effectauthor.ID2D1ResourceTexture.Update
title: ID2D1ResourceTexture::Update (d2d1effectauthor.h)
description: Updates the specific resource texture inside the specific range or box using the supplied data.
helpviewer_keywords: ["ID2D1ResourceTexture interface [Direct2D]","Update method","ID2D1ResourceTexture.Update","ID2D1ResourceTexture::Update","Update","Update method [Direct2D]","Update method [Direct2D]","ID2D1ResourceTexture interface","d2d1effectauthor/ID2D1ResourceTexture::Update","direct2d.id2d1resourcetexture_update"]
old-location: direct2d\id2d1resourcetexture_update.htm
tech.root: Direct2D
ms.assetid: B2E36886-DAD5-47EA-9252-541283064D98
ms.date: 12/05/2018
ms.keywords: ID2D1ResourceTexture interface [Direct2D],Update method, ID2D1ResourceTexture.Update, ID2D1ResourceTexture::Update, Update, Update method [Direct2D], Update method [Direct2D],ID2D1ResourceTexture interface, d2d1effectauthor/ID2D1ResourceTexture::Update, direct2d.id2d1resourcetexture_update
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
req.lib: D2d1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1ResourceTexture::Update
 - d2d1effectauthor/ID2D1ResourceTexture::Update
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1ResourceTexture.Update
---

# ID2D1ResourceTexture::Update


## -description

Updates the specific resource texture inside the specific range or box using the supplied data.

## -parameters

### -param minimumExtents [in, optional]

Type: <b>const UINT32*</b>

The "left" extent of the updates if specified; if <b>NULL</b>, the entire texture is updated.

### -param maximimumExtents [in, optional]

Type: <b>const UINT32*</b>

The "right" extent of the updates if specified; if <b>NULL</b>, the entire texture is updated.

### -param strides [in]

Type: <b>const UINT32*</b>

The stride to advance through the input data, according to dimension.

### -param dimensions

Type: <b>UINT32</b>

The number of dimensions in the resource texture. This must match the number used to load the texture.

### -param data [in]

Type: <b>const BYTE*</b>

The data to be placed into the resource texture.

### -param dataCount

Type: <b>UINT32</b>

The size of the data buffer to be used to update the resource texture.

## -returns

Type: <b>HRESULT</b>

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.


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
<td> E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>

## -remarks

The number of dimensions in the update must match those of the created texture.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createresourcetexture">ID2D1EffectContext::CreateResourceTexture</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1resourcetexture">ID2D1ResourceTexture</a>