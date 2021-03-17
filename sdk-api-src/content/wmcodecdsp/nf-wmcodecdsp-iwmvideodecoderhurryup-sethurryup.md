---
UID: NF:wmcodecdsp.IWMVideoDecoderHurryup.SetHurryup
title: IWMVideoDecoderHurryup::SetHurryup (wmcodecdsp.h)
description: Sets the speed mode of the video decoder.
helpviewer_keywords: ["IWMVideoDecoderHurryup interface [Media Foundation]","SetHurryup method","IWMVideoDecoderHurryup.SetHurryup","IWMVideoDecoderHurryup::SetHurryup","SetHurryup","SetHurryup method [Media Foundation]","SetHurryup method [Media Foundation]","IWMVideoDecoderHurryup interface","codecapi.iwmvideodecoderhurryupsethurryup","mf.iwmvideodecoderhurryupsethurryup","wmcodecdsp/IWMVideoDecoderHurryup::SetHurryup"]
old-location: mf\iwmvideodecoderhurryupsethurryup.htm
tech.root: mf
ms.assetid: ef01d2ab-2525-4caf-87d9-3acdc0b3b1b3
ms.date: 12/05/2018
ms.keywords: IWMVideoDecoderHurryup interface [Media Foundation],SetHurryup method, IWMVideoDecoderHurryup.SetHurryup, IWMVideoDecoderHurryup::SetHurryup, SetHurryup, SetHurryup method [Media Foundation], SetHurryup method [Media Foundation],IWMVideoDecoderHurryup interface, codecapi.iwmvideodecoderhurryupsethurryup, mf.iwmvideodecoderhurryupsethurryup, wmcodecdsp/IWMVideoDecoderHurryup::SetHurryup
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
 - IWMVideoDecoderHurryup::SetHurryup
 - wmcodecdsp/IWMVideoDecoderHurryup::SetHurryup
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
 - IWMVideoDecoderHurryup.SetHurryup
---

# IWMVideoDecoderHurryup::SetHurryup


## -description

Sets the speed mode of the video decoder.

## -parameters

### -param lHurryup [in]

The speed mode of the video decoder.

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
The decoder will decode faster than real time. The higher the value, the faster the decoding.

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

<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmvideodecoderhurryup-gethurryup">IWMVideoDecoderHurryUp::GetHurryup</a>



<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderhurryup">IWMVideoDecoderHurryup Interface</a>