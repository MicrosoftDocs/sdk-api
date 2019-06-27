---
UID: NN:control.IQueueCommand
title: IQueueCommand (control.h)
author: windows-sdk-content
description: The IQueueCommand interface queues a command for processing at a designated time.
old-location: dshow\iqueuecommand.htm
tech.root: DirectShow
ms.assetid: 08efcbec-ce17-44e8-a3c1-4b5b95dcaaa4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IQueueCommand, IQueueCommand interface [DirectShow], IQueueCommand interface [DirectShow],described, IQueueCommandInterface, control/IQueueCommand, dshow.iqueuecommand
ms.topic: interface
f1_keywords: 
 - "control/IQueueCommand"
req.header: control.h
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
 - IQueueCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IQueueCommand interface


## -description



The <code>IQueueCommand</code> interface queues a command for processing at a designated time. The Filter Graph Manager exposes this interface. Applications can use it to queue graph-control commands in advance.

The methods in <code>IQueueCommand</code> are modeled after the <b>IDispatch::InvokeAt</b> method. The application specifies an interface, a method on the interface, parameters to the method, and a reference time. The Filter Graph Manager queues this information and then invokes the method at the specified time. The requested interface must inherit <b>IDispatch</b> and must be exposed by the Filter Graph Manager. Examples include <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl</a>, <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition</a>.

When the command is queued, the filter graph manager returns a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ideferredcommand">IDeferredCommand</a> interface. The application can use this interface to cancel or modify the command.

<div class="alert"><b>Note</b>  The two methods in <code>IQueueCommand</code> refer to stream time and presentation time, respectively. In the context of the Filter Graph Manager, stream time and presentation time are identical, so there is no functional difference between the two methods. Other objects could implement <code>IQueueCommand</code> differently. For more information about stream time and presentation time, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/time-and-clocks-in-directshow">Time and Clocks in DirectShow</a>.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueueCommand</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQueueCommand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQueueCommand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-iqueuecommand-invokeatpresentationtime">InvokeAtPresentationTime</a>
</td>
<td align="left" width="63%">
Queues a method to be invoked at the specified presentation time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-iqueuecommand-invokeatstreamtime">InvokeAtStreamTime</a>
</td>
<td align="left" width="63%">
Queues a method to be invoked at the specified stream time.

</td>
</tr>
</table> 

