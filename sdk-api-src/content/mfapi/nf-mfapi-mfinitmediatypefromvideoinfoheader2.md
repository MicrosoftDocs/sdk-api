---
UID: NF:mfapi.MFInitMediaTypeFromVideoInfoHeader2
title: MFInitMediaTypeFromVideoInfoHeader2 function (mfapi.h)
description: Initializes a media type from a DirectShow VIDEOINFOHEADER2 structure.
helpviewer_keywords: ["4077ae40-75b2-4c45-b62e-740e216ebf89","MFInitMediaTypeFromVideoInfoHeader2","MFInitMediaTypeFromVideoInfoHeader2 function [Media Foundation]","mf.mfinitmediatypefromvideoinfoheader2","mfapi/MFInitMediaTypeFromVideoInfoHeader2"]
old-location: mf\mfinitmediatypefromvideoinfoheader2.htm
tech.root: mf
ms.assetid: 4077ae40-75b2-4c45-b62e-740e216ebf89
ms.date: 12/05/2018
ms.keywords: 4077ae40-75b2-4c45-b62e-740e216ebf89, MFInitMediaTypeFromVideoInfoHeader2, MFInitMediaTypeFromVideoInfoHeader2 function [Media Foundation], mf.mfinitmediatypefromvideoinfoheader2, mfapi/MFInitMediaTypeFromVideoInfoHeader2
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
 - MFInitMediaTypeFromVideoInfoHeader2
 - mfapi/MFInitMediaTypeFromVideoInfoHeader2
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
 - MFInitMediaTypeFromVideoInfoHeader2
---

# MFInitMediaTypeFromVideoInfoHeader2 function


## -description

Initializes a media type from a DirectShow <b>VIDEOINFOHEADER2</b> structure.

## -parameters

### -param pMFType

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type to initialize. To create the uninitialized media type object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a>.

### -param pVIH2

Pointer to a <b>VIDEOINFOHEADER2</b> structure that describes the media type. The caller must fill in the structure members before calling this function.

### -param cbBufSize

Size of the <b>VIDEOINFOHEADER2</b> structure, in bytes.

### -param pSubtype

Pointer to a subtype GUID. This parameter can be <b>NULL</b>. If the subtype GUID is specified, the function uses it to set the media subtype. Otherwise, the function attempts to deduce the subtype from the <b>biCompression</b> field contained in the <b>VIDEOINFOHEADER2</b> structure.

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

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-type-conversions">Media Type Conversions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>