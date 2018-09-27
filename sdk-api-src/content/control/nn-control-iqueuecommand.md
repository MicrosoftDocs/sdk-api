---
UID: NN:control.IQueueCommand
title: IQueueCommand
author: windows-sdk-content
description: The IQueueCommand interface queues a command for processing at a designated time.
old-location: dshow\iqueuecommand.htm
tech.root: DirectShow
ms.assetid: 08efcbec-ce17-44e8-a3c1-4b5b95dcaaa4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IQueueCommand, IQueueCommand interface [DirectShow], IQueueCommand interface [DirectShow],described, IQueueCommandInterface, control/IQueueCommand, dshow.iqueuecommand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IQueueCommand interface


## -description



The <code>IQueueCommand</code> interface queues a command for processing at a designated time. The Filter Graph Manager exposes this interface. Applications can use it to queue graph-control commands in advance.

The methods in <code>IQueueCommand</code> are modeled after the <b>IDispatch::InvokeAt</b> method. The application specifies an interface, a method on the interface, parameters to the method, and a reference time. The Filter Graph Manager queues this information and then invokes the method at the specified time. The requested interface must inherit <b>IDispatch</b> and must be exposed by the Filter Graph Manager. Examples include <a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl</a>, <a href="https://msdn.microsoft.com/9d367b0a-c7ec-49d4-a41e-045ac81d2c51">IMediaEventEx</a>, and <a href="https://msdn.microsoft.com/325dd9a4-80ca-43e3-9ff8-473df1b833e9">IMediaPosition</a>.

When the command is queued, the filter graph manager returns a pointer to the <a href="https://msdn.microsoft.com/8161932a-16aa-4700-b91d-b4d8948ad59f">IDeferredCommand</a> interface. The application can use this interface to cancel or modify the command.

<div class="alert"><b>Note</b>  The two methods in <code>IQueueCommand</code> refer to stream time and presentation time, respectively. In the context of the Filter Graph Manager, stream time and presentation time are identical, so there is no functional difference between the two methods. Other objects could implement <code>IQueueCommand</code> differently. For more information about stream time and presentation time, see <a href="https://msdn.microsoft.com/7d883638-5ddb-48b9-9d0b-104944a151e9">Time and Clocks in DirectShow</a>.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueueCommand</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IQueueCommand</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/95255a18-d6e3-4970-90cb-c87629560ff6">InvokeAtPresentationTime</a>
</td>
<td align="left" width="63%">
Queues a method to be invoked at the specified presentation time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/350b6842-207c-47db-a3f8-9e2784d9da67">InvokeAtStreamTime</a>
</td>
<td align="left" width="63%">
Queues a method to be invoked at the specified stream time.

</td>
</tr>
</table> 

