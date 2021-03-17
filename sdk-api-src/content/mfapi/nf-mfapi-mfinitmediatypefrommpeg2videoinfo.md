---
UID: NF:mfapi.MFInitMediaTypeFromMPEG2VideoInfo
title: MFInitMediaTypeFromMPEG2VideoInfo function (mfapi.h)
description: Initializes a media type from a DirectShow MPEG2VIDEOINFO structure.
helpviewer_keywords: ["44ad976e-2b15-454c-9422-26fc960e03aa","MFInitMediaTypeFromMPEG2VideoInfo","MFInitMediaTypeFromMPEG2VideoInfo function [Media Foundation]","mf.mfinitmediatypefrommpeg2videoinfo","mfapi/MFInitMediaTypeFromMPEG2VideoInfo"]
old-location: mf\mfinitmediatypefrommpeg2videoinfo.htm
tech.root: mf
ms.assetid: 44ad976e-2b15-454c-9422-26fc960e03aa
ms.date: 12/05/2018
ms.keywords: 44ad976e-2b15-454c-9422-26fc960e03aa, MFInitMediaTypeFromMPEG2VideoInfo, MFInitMediaTypeFromMPEG2VideoInfo function [Media Foundation], mf.mfinitmediatypefrommpeg2videoinfo, mfapi/MFInitMediaTypeFromMPEG2VideoInfo
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
 - MFInitMediaTypeFromMPEG2VideoInfo
 - mfapi/MFInitMediaTypeFromMPEG2VideoInfo
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
 - MFInitMediaTypeFromMPEG2VideoInfo
---

# MFInitMediaTypeFromMPEG2VideoInfo function


## -description

Initializes a media type from a DirectShow <b>MPEG2VIDEOINFO</b> structure.

## -parameters

### -param pMFType

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type to initialize. To create the uninitialized media type object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a>.

### -param pMP2VI

Pointer to a <b>MPEG2VIDEOINFO</b> structure that describes the media type. The caller must fill in the structure members before calling this function.

### -param cbBufSize

Size of the <b>MPEG2VIDEOINFO</b> structure, in bytes.

### -param pSubtype

Pointer to a subtype GUID. This parameter can be <b>NULL</b>. If the subtype GUID is specified, the function uses it to set the media subtype. Otherwise, the function attempts to deduce the subtype from the <b>biCompression</b> field contained in the <b>MPEG2VIDEOINFO</b> structure.

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