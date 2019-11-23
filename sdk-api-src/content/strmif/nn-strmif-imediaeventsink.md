---
UID: NN:strmif.IMediaEventSink
title: IMediaEventSink (strmif.h)

description: Notifies the Filter Graph Manager of events that occur within the filter graph.
old-location: dshow\imediaeventsink.htm
tech.root: DirectShow
ms.assetid: 50aa04b4-9a04-4d0d-a558-42595a69aef7

ms.date: 12/05/2018
ms.keywords: IMediaEventSink, IMediaEventSink interface [DirectShow], IMediaEventSink interface [DirectShow],described, IMediaEventSinkInterface, dshow.imediaeventsink, strmif/IMediaEventSink
ms.topic: interface
f1_keywords: 
 - "strmif/IMediaEventSink"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaEventSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaEventSink interface


## -description



Notifies the Filter Graph Manager of events that occur within the filter graph. Filters use this interface to report events. The Filter Graph Manager exposes this interface.

Applications do not use <code>IMediaEventSink</code>. To retrieve events, applications use the <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaeventsink-notify">Notify</a>
</td>
<td align="left" width="63%">
Notifies the Filter Graph Manager of an event.

</td>
</tr>
</table> 

