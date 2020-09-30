---
UID: NN:sbe.IStreamBufferSource
title: IStreamBufferSource (sbe.h)
description: The IStreamBufferSource interface is exposed by the Stream Buffer Source filter. Use this interface to play live content from the Stream Buffer Sink filter.
helpviewer_keywords: ["IStreamBufferSource","IStreamBufferSource interface [Microsoft TV Technologies]","IStreamBufferSource interface [Microsoft TV Technologies]","described","IStreamBufferSourceInterface","mstv.istreambuffersource","sbe/IStreamBufferSource"]
old-location: mstv\istreambuffersource.htm
tech.root: mstv
ms.assetid: 1e407f85-820a-4d17-926d-0c00e1e453e2
ms.date: 12/05/2018
ms.keywords: IStreamBufferSource, IStreamBufferSource interface [Microsoft TV Technologies], IStreamBufferSource interface [Microsoft TV Technologies],described, IStreamBufferSourceInterface, mstv.istreambuffersource, sbe/IStreamBufferSource
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IStreamBufferSource
 - sbe/IStreamBufferSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferSource
---

# IStreamBufferSource interface


## -description

The <b>IStreamBufferSource</b> interface is exposed by the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter. Use this interface to play live content from the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-sink-filter">Stream Buffer Sink</a> filter.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferSource</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersource-setstreamsink">SetStreamSink</a>
</td>
<td align="left" width="63%">
Sets a pointer to the Stream Buffer Sink filter, so that the source filter can stream data from the sink filter.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferSource)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>



<a href="/previous-versions/windows/desktop/mstv/using-the-stream-buffer-engine">Using the Stream Buffer Engine</a>