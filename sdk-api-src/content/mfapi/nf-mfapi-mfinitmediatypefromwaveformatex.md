---
UID: NF:mfapi.MFInitMediaTypeFromWaveFormatEx
title: MFInitMediaTypeFromWaveFormatEx function (mfapi.h)
description: Initializes a media type from a WAVEFORMATEX structure.
helpviewer_keywords: ["91a201a6-06cf-4445-ad62-fdabb3848d51","MFInitMediaTypeFromWaveFormatEx","MFInitMediaTypeFromWaveFormatEx function [Media Foundation]","mf.mfinitmediatypefromwaveformatex","mfapi/MFInitMediaTypeFromWaveFormatEx"]
old-location: mf\mfinitmediatypefromwaveformatex.htm
tech.root: mf
ms.assetid: 91a201a6-06cf-4445-ad62-fdabb3848d51
ms.date: 12/05/2018
ms.keywords: 91a201a6-06cf-4445-ad62-fdabb3848d51, MFInitMediaTypeFromWaveFormatEx, MFInitMediaTypeFromWaveFormatEx function [Media Foundation], mf.mfinitmediatypefromwaveformatex, mfapi/MFInitMediaTypeFromWaveFormatEx
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFInitMediaTypeFromWaveFormatEx
 - mfapi/MFInitMediaTypeFromWaveFormatEx
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
 - MFInitMediaTypeFromWaveFormatEx
---

# MFInitMediaTypeFromWaveFormatEx function


## -description

Initializes a media type from a <b>WAVEFORMATEX</b> structure.

## -parameters

### -param pMFType

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type to initialize. To create the uninitialized media type object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a>.

### -param pWaveFormat

Pointer to a <b>WAVEFORMATEX</b> structure that describes the media type. The caller must fill in the structure members before calling this function.

### -param cbBufSize

Size of the <b>WAVEFORMATEX</b> structure, in bytes.

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