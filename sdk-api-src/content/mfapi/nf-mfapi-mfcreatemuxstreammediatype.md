---
UID: NF:mfapi.MFCreateMuxStreamMediaType
title: MFCreateMuxStreamMediaType function (mfapi.h)
description: Creates an IMFMediaType describing the media types of multiplexed substreams.
helpviewer_keywords: ["MFCreateMuxStreamMediaType","MFCreateMuxStreamMediaType function [Media Foundation]","mf.mfcreatemuxstreammediatype","mfapi/MFCreateMuxStreamMediaType"]
old-location: mf\mfcreatemuxstreammediatype.htm
tech.root: mf
ms.assetid: 27E1295C-BFB1-45EB-ABB2-DDFF927F6E30
ms.date: 12/05/2018
ms.keywords: MFCreateMuxStreamMediaType, MFCreateMuxStreamMediaType function [Media Foundation], mf.mfcreatemuxstreammediatype, mfapi/MFCreateMuxStreamMediaType
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - MFCreateMuxStreamMediaType
 - mfapi/MFCreateMuxStreamMediaType
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
 - MFCreateMuxStreamMediaType
---

# MFCreateMuxStreamMediaType function


## -description

Creates an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> describing the media types  of multiplexed substreams.

## -parameters

### -param pMediaTypesToMux [in]

The collection containing the  <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> for each multiplexed substream.

### -param ppMuxMediaType [out]

The <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> containing the media types for the multiplexed substreams.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pMediaTypesToMux</i> parameter in null.

</td>
</tr>
</table>