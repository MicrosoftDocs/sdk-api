---
UID: NF:evr.IEVRFilterConfig.GetNumberOfStreams
title: IEVRFilterConfig::GetNumberOfStreams (evr.h)
description: Retrieves the number of input pins on the EVR filter. The EVR filter always has at least one input pin, which corresponds to the reference stream.
helpviewer_keywords: ["94e15032-efb6-4919-b018-953eee803135","GetNumberOfStreams","GetNumberOfStreams method [Media Foundation]","GetNumberOfStreams method [Media Foundation]","IEVRFilterConfig interface","IEVRFilterConfig interface [Media Foundation]","GetNumberOfStreams method","IEVRFilterConfig.GetNumberOfStreams","IEVRFilterConfig::GetNumberOfStreams","evr/IEVRFilterConfig::GetNumberOfStreams","mf.ievrfilterconfig_getnumberofstreams"]
old-location: mf\ievrfilterconfig_getnumberofstreams.htm
tech.root: mf
ms.assetid: 94e15032-efb6-4919-b018-953eee803135
ms.date: 12/05/2018
ms.keywords: 94e15032-efb6-4919-b018-953eee803135, GetNumberOfStreams, GetNumberOfStreams method [Media Foundation], GetNumberOfStreams method [Media Foundation],IEVRFilterConfig interface, IEVRFilterConfig interface [Media Foundation],GetNumberOfStreams method, IEVRFilterConfig.GetNumberOfStreams, IEVRFilterConfig::GetNumberOfStreams, evr/IEVRFilterConfig::GetNumberOfStreams, mf.ievrfilterconfig_getnumberofstreams
req.header: evr.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEVRFilterConfig::GetNumberOfStreams
 - evr/IEVRFilterConfig::GetNumberOfStreams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IEVRFilterConfig.GetNumberOfStreams
---

# IEVRFilterConfig::GetNumberOfStreams


## -description

Retrieves the number of input pins on the EVR filter. The EVR filter always has at least one input pin, which corresponds to the reference stream.

## -parameters

### -param pdwMaxStreams [out]

Receives the number of streams.

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

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig">IEVRFilterConfig</a>