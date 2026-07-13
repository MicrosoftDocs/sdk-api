---
UID: NF:d2d1_1.ID2D1ColorContext.GetProfile
title: ID2D1ColorContext::GetProfile (d2d1_1.h)
description: Gets the color profile bytes for an ID2D1ColorContext.
helpviewer_keywords: ["GetProfile","GetProfile method [Direct2D]","GetProfile method [Direct2D]","ID2D1ColorContext interface","ID2D1ColorContext interface [Direct2D]","GetProfile method","ID2D1ColorContext.GetProfile","ID2D1ColorContext::GetProfile","d2d1_1/ID2D1ColorContext::GetProfile","direct2d.id2d1colorcontext_getprofile"]
old-location: direct2d\id2d1colorcontext_getprofile.htm
tech.root: Direct2D
ms.assetid: f6beae12-e02d-432b-b9d8-5e1206e3c482
ms.date: 12/05/2018
ms.keywords: GetProfile, GetProfile method [Direct2D], GetProfile method [Direct2D],ID2D1ColorContext interface, ID2D1ColorContext interface [Direct2D],GetProfile method, ID2D1ColorContext.GetProfile, ID2D1ColorContext::GetProfile, d2d1_1/ID2D1ColorContext::GetProfile, direct2d.id2d1colorcontext_getprofile
req.header: d2d1_1.h
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1ColorContext::GetProfile
 - d2d1_1/ID2D1ColorContext::GetProfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1ColorContext.GetProfile
---

# ID2D1ColorContext::GetProfile


## -description

Gets the color profile bytes for an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a>.

## -parameters

### -param profile [out]

Type: <b>BYTE*</b>

When this method returns, contains the color profile.

### -param profileSize

Type: <b>UINT32</b>

The size of the <i>profile</i> buffer.

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
<td>D2DERR_INSUFFICIENT_BUFFER</td>
<td>The supplied buffer was too small to accommodate the data.</td>
</tr>
</table>

## -remarks

If <i>profileSize</i> is insufficient to store the entire profile, <i>profile</i> is zero-initialized before this method fails.

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getcolorcontext">ID2D1Bitmap1::GetColorContext</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1colorcontext-getprofilesize">ID2D1ColorContext::GetProfileSize</a>