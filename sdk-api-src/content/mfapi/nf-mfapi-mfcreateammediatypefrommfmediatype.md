---
UID: NF:mfapi.MFCreateAMMediaTypeFromMFMediaType
title: MFCreateAMMediaTypeFromMFMediaType function (mfapi.h)
description: Creates a DirectShow AM_MEDIA_TYPE structure from a Media Foundation media type.
helpviewer_keywords: ["53b191d4-89b3-4b16-8f89-50f256689e85","MFCreateAMMediaTypeFromMFMediaType","MFCreateAMMediaTypeFromMFMediaType function [Media Foundation]","mf.mfcreateammediatypefrommfmediatype","mfapi/MFCreateAMMediaTypeFromMFMediaType"]
old-location: mf\mfcreateammediatypefrommfmediatype.htm
tech.root: mf
ms.assetid: 53b191d4-89b3-4b16-8f89-50f256689e85
ms.date: 12/05/2018
ms.keywords: 53b191d4-89b3-4b16-8f89-50f256689e85, MFCreateAMMediaTypeFromMFMediaType, MFCreateAMMediaTypeFromMFMediaType function [Media Foundation], mf.mfcreateammediatypefrommfmediatype, mfapi/MFCreateAMMediaTypeFromMFMediaType
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
 - MFCreateAMMediaTypeFromMFMediaType
 - mfapi/MFCreateAMMediaTypeFromMFMediaType
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
 - MFCreateAMMediaTypeFromMFMediaType
---

# MFCreateAMMediaTypeFromMFMediaType function


## -description

Creates a DirectShow <b>AM_MEDIA_TYPE</b> structure from a Media Foundation media type.

## -parameters

### -param pMFType

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type to convert.

### -param guidFormatBlockType

Format type GUID. This value corresponds to the <b>formattype</b> member of the <b>AM_MEDIA_TYPE</b> structure and specifies the type of format block to allocate. If the value is GUID_NULL, the function attempts to deduce the correct format block, based on the major type and subtype.

### -param ppAMType

Receives a pointer to an <b>AM_MEDIA_TYPE</b> structure. The caller must release the memory allocated for the structure by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. The function also allocates memory for the format block, which the caller must release by calling <b>CoTaskMemFree</b> on the <b>pbFormat</b> member.

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