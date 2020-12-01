---
UID: NF:mfapi.MFInitMediaTypeFromAMMediaType
title: MFInitMediaTypeFromAMMediaType function (mfapi.h)
description: Initializes a media type from a DirectShow AM_MEDIA_TYPE structure.
helpviewer_keywords: ["MFInitMediaTypeFromAMMediaType","MFInitMediaTypeFromAMMediaType function [Media Foundation]","da5dcc32-c027-4b9a-b72f-a60b98885636","mf.mfinitmediatypefromammediatype","mfapi/MFInitMediaTypeFromAMMediaType"]
old-location: mf\mfinitmediatypefromammediatype.htm
tech.root: mf
ms.assetid: da5dcc32-c027-4b9a-b72f-a60b98885636
ms.date: 12/05/2018
ms.keywords: MFInitMediaTypeFromAMMediaType, MFInitMediaTypeFromAMMediaType function [Media Foundation], da5dcc32-c027-4b9a-b72f-a60b98885636, mf.mfinitmediatypefromammediatype, mfapi/MFInitMediaTypeFromAMMediaType
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFInitMediaTypeFromAMMediaType
 - mfapi/MFInitMediaTypeFromAMMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFInitMediaTypeFromAMMediaType
---

# MFInitMediaTypeFromAMMediaType function


## -description

Initializes a media type from a DirectShow <b>AM_MEDIA_TYPE</b> structure.

## -parameters

### -param pMFType

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type to initialize. To create the uninitialized media type object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a>.

### -param pAMType

Pointer to an <b>AM_MEDIA_TYPE</b> structure that describes the media type. The caller must fill in the structure members before calling this function.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -remarks

This function can also be used with the following format structures that are equivalent to <b>AM_MEDIA_TYPE</b>:

<ul>
<li>
<b>DMO_MEDIA_TYPE</b> (DirectX Media Objects)

</li>
<li>
<b>WM_MEDIA_TYPE</b> (Windows Media Format SDK)

</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-type-conversions">Media Type Conversions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>