---
UID: NF:mfapi.MFCreateMuxStreamSample
title: MFCreateMuxStreamSample function (mfapi.h)
description: Creates an IMFSample containing the samples of multiplexed substreams.
helpviewer_keywords: ["MFCreateMuxStreamSample","MFCreateMuxStreamSample function [Media Foundation]","mf.mfcreatemuxstreamsample","mfapi/MFCreateMuxStreamSample"]
old-location: mf\mfcreatemuxstreamsample.htm
tech.root: mf
ms.assetid: D7E7B260-54E0-47F4-9762-ADB06103CDF3
ms.date: 12/05/2018
ms.keywords: MFCreateMuxStreamSample, MFCreateMuxStreamSample function [Media Foundation], mf.mfcreatemuxstreamsample, mfapi/MFCreateMuxStreamSample
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
 - MFCreateMuxStreamSample
 - mfapi/MFCreateMuxStreamSample
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
 - MFCreateMuxStreamSample
---

# MFCreateMuxStreamSample function


## -description

Creates an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> containing the samples of multiplexed substreams.

## -parameters

### -param pSamplesToMux [in]

The collection containing the  <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> for each multiplexed substream.

### -param ppMuxSample [out]

The <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> containing the samples for the multiplexed substreams.

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
The <i>pSamplesToMux</i> parameter in null.

</td>
</tr>
</table>