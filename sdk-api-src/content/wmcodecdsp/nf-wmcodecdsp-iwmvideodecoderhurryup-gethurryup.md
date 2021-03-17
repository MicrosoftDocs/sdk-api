---
UID: NF:wmcodecdsp.IWMVideoDecoderHurryup.GetHurryup
title: IWMVideoDecoderHurryup::GetHurryup (wmcodecdsp.h)
description: Retrieves the current speed mode of the video decoder.
helpviewer_keywords: ["GetHurryup","GetHurryup method [Media Foundation]","GetHurryup method [Media Foundation]","IWMVideoDecoderHurryup interface","IWMVideoDecoderHurryup interface [Media Foundation]","GetHurryup method","IWMVideoDecoderHurryup.GetHurryup","IWMVideoDecoderHurryup::GetHurryup","codecapi.iwmvideodecoderhurryupgethurryup","mf.iwmvideodecoderhurryupgethurryup","wmcodecdsp/IWMVideoDecoderHurryup::GetHurryup"]
old-location: mf\iwmvideodecoderhurryupgethurryup.htm
tech.root: mf
ms.assetid: c5c58acd-ebf9-46ce-977b-1478b42559c4
ms.date: 12/05/2018
ms.keywords: GetHurryup, GetHurryup method [Media Foundation], GetHurryup method [Media Foundation],IWMVideoDecoderHurryup interface, IWMVideoDecoderHurryup interface [Media Foundation],GetHurryup method, IWMVideoDecoderHurryup.GetHurryup, IWMVideoDecoderHurryup::GetHurryup, codecapi.iwmvideodecoderhurryupgethurryup, mf.iwmvideodecoderhurryupgethurryup, wmcodecdsp/IWMVideoDecoderHurryup::GetHurryup
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMVideoDecoderHurryup::GetHurryup
 - wmcodecdsp/IWMVideoDecoderHurryup::GetHurryup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMVideoDecoderHurryup.GetHurryup
---

# IWMVideoDecoderHurryup::GetHurryup


## -description

Retrieves the current speed mode of the video decoder.

## -parameters

### -param plHurryup [out]

Address of a variable that receives the decoder speed mode.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1 (default)</dt>
</dl>
</td>
<td width="60%">
The decoder will determine the decoding speed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The decoder will decode in real time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1 to 4</dt>
</dl>
</td>
<td width="60%">
The decoder will decode faster than real time.

</td>
</tr>
</table>

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmvideodecoderhurryup-sethurryup">IWMVideoDecoderHurryUp::SetHurryup</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderhurryup">IWMVideoDecoderHurryup Interface</a>