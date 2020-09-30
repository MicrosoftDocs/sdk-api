---
UID: NF:mfapi.MFCreateWaveFormatExFromMFMediaType
title: MFCreateWaveFormatExFromMFMediaType function (mfapi.h)
description: Converts a Media Foundation audio media type to a WAVEFORMATEX structure.
helpviewer_keywords: ["MFCreateWaveFormatExFromMFMediaType","MFCreateWaveFormatExFromMFMediaType function [Media Foundation]","b124bac2-90de-4358-a079-f509a89c3776","mf.mfcreatewaveformatexfrommfmediatype","mfapi/MFCreateWaveFormatExFromMFMediaType"]
old-location: mf\mfcreatewaveformatexfrommfmediatype.htm
tech.root: mf
ms.assetid: b124bac2-90de-4358-a079-f509a89c3776
ms.date: 12/05/2018
ms.keywords: MFCreateWaveFormatExFromMFMediaType, MFCreateWaveFormatExFromMFMediaType function [Media Foundation], b124bac2-90de-4358-a079-f509a89c3776, mf.mfcreatewaveformatexfrommfmediatype, mfapi/MFCreateWaveFormatExFromMFMediaType
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
 - MFCreateWaveFormatExFromMFMediaType
 - mfapi/MFCreateWaveFormatExFromMFMediaType
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
 - MFCreateWaveFormatExFromMFMediaType
---

# MFCreateWaveFormatExFromMFMediaType function


## -description

Converts a Media Foundation audio media type to a <b>WAVEFORMATEX</b> structure.

## -parameters

### -param pMFType

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type.

### -param ppWF

Receives a pointer to the <b>WAVEFORMATEX</b> structure. The caller must release the memory allocated for the structure by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pcbSize

Receives the size of the <b>WAVEFORMATEX</b> structure.

### -param Flags

Contains a flag from the <a href="/windows/desktop/api/mfapi/ne-mfapi-mfwaveformatexconvertflags">MFWaveFormatExConvertFlags</a> enumeration.

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

If the <b>wFormatTag</b> member of the returned structure is <b>WAVE_FORMAT_EXTENSIBLE</b>, you can cast the pointer to a <b>WAVEFORMATEXTENSIBLE</b> structure.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-type-conversions">Media Type Conversions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>