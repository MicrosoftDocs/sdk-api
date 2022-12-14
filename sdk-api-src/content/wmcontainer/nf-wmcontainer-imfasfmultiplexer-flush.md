---
UID: NF:wmcontainer.IMFASFMultiplexer.Flush
title: IMFASFMultiplexer::Flush (wmcontainer.h)
description: Signals the multiplexer to process all queued output media samples. Call this method after passing the last sample to the multiplexer.
helpviewer_keywords: ["44a66374-ad9d-4c76-8c95-21a15e071c6d","Flush","Flush method [Media Foundation]","Flush method [Media Foundation]","IMFASFMultiplexer interface","IMFASFMultiplexer interface [Media Foundation]","Flush method","IMFASFMultiplexer.Flush","IMFASFMultiplexer::Flush","mf.imfasfmultiplexer_flush","wmcontainer/IMFASFMultiplexer::Flush"]
old-location: mf\imfasfmultiplexer_flush.htm
tech.root: mf
ms.assetid: 44a66374-ad9d-4c76-8c95-21a15e071c6d
ms.date: 12/05/2018
ms.keywords: 44a66374-ad9d-4c76-8c95-21a15e071c6d, Flush, Flush method [Media Foundation], Flush method [Media Foundation],IMFASFMultiplexer interface, IMFASFMultiplexer interface [Media Foundation],Flush method, IMFASFMultiplexer.Flush, IMFASFMultiplexer::Flush, mf.imfasfmultiplexer_flush, wmcontainer/IMFASFMultiplexer::Flush
req.header: wmcontainer.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFMultiplexer::Flush
 - wmcontainer/IMFASFMultiplexer::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFMultiplexer.Flush
---

# IMFASFMultiplexer::Flush


## -description

Signals the multiplexer to process all queued output media samples. Call this method after passing the last sample to the multiplexer.



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

You must call <b>Flush</b> after the last sample has been passed into the ASF multiplexer and before you call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end">IMFASFMultiplexer::End</a>. This causes all output media samples in progress to be completed. After calling <b>Flush</b>, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket">IMFASFMultiplexer::GetNextPacket</a> in a loop until all the pending media samples have been packetized.

## -see-also

<a href="/windows/desktop/medfound/generating-new-asf-data-packets">Generating New ASF Data Packets</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer">IMFASFMultiplexer</a>
