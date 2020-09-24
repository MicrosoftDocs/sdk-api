---
UID: NF:wmcodecdsp.IWMCodecOutputTimestamp.GetNextOutputTime
title: IWMCodecOutputTimestamp::GetNextOutputTime (wmcodecdsp.h)
description: Queries the decoder for the time stamp of the upcoming output sample. Use this method if you need to know the time of the sample before calling IMediaObject::ProcessOutput or IMFTransform::ProcessOutput to get the sample.
helpviewer_keywords: ["GetNextOutputTime","GetNextOutputTime method [Media Foundation]","GetNextOutputTime method [Media Foundation]","IWMCodecOutputTimestamp interface","IWMCodecOutputTimestamp interface [Media Foundation]","GetNextOutputTime method","IWMCodecOutputTimestamp.GetNextOutputTime","IWMCodecOutputTimestamp::GetNextOutputTime","codecapi.iwmcodecoutputtimestampgetnextoutputtime","mf.iwmcodecoutputtimestampgetnextoutputtime","wmcodecdsp/IWMCodecOutputTimestamp::GetNextOutputTime"]
old-location: mf\iwmcodecoutputtimestampgetnextoutputtime.htm
tech.root: mf
ms.assetid: 8af7e77b-da10-4d6a-b7a1-515a54aa3a20
ms.date: 12/05/2018
ms.keywords: GetNextOutputTime, GetNextOutputTime method [Media Foundation], GetNextOutputTime method [Media Foundation],IWMCodecOutputTimestamp interface, IWMCodecOutputTimestamp interface [Media Foundation],GetNextOutputTime method, IWMCodecOutputTimestamp.GetNextOutputTime, IWMCodecOutputTimestamp::GetNextOutputTime, codecapi.iwmcodecoutputtimestampgetnextoutputtime, mf.iwmcodecoutputtimestampgetnextoutputtime, wmcodecdsp/IWMCodecOutputTimestamp::GetNextOutputTime
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
 - IWMCodecOutputTimestamp::GetNextOutputTime
 - wmcodecdsp/IWMCodecOutputTimestamp::GetNextOutputTime
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
 - IWMCodecOutputTimestamp.GetNextOutputTime
---

# IWMCodecOutputTimestamp::GetNextOutputTime


## -description

Queries the decoder for the time stamp of the upcoming output sample. Use this method if you need to know the time of the sample before calling <b>IMediaObject::ProcessOutput</b> or <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a> to get the sample.

## -parameters

### -param prtTime [out]

Address of a variable that receives the presentation time of the next sample.

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

## -remarks

This method is important when decoding video using frame interpolation, because the rendering application cannot predict the time stamps of interpolated frames.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecoutputtimestamp">IWMCodecOutputTimestamp Interface</a>