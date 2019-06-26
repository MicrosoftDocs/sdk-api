---
UID: NN:control.IDeferredCommand
title: IDeferredCommand (control.h)
author: windows-sdk-content
description: The IDeferredCommand interface cancels or modify graph-control commands that were queued using the IQueueCommand interface.When an application calls an IQueueCommand method on the Filter Graph Manager, it receives a pointer to the IDeferredCommand interface. The application can use the interface to cancel or postpone the command, or retrieve the return value from the command.
old-location: dshow\ideferredcommand.htm
tech.root: DirectShow
ms.assetid: 8161932a-16aa-4700-b91d-b4d8948ad59f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDeferredCommand, IDeferredCommand interface [DirectShow], IDeferredCommand interface [DirectShow],described, IDeferredCommandInterface, control/IDeferredCommand, dshow.ideferredcommand
ms.topic: interface
f1_keywords: 
 - "control/IDeferredCommand"
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
 - IDeferredCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDeferredCommand interface


## -description



The <code>IDeferredCommand</code> interface cancels or modify graph-control commands that were queued using the <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-iqueuecommand">IQueueCommand</a> interface.

When an application calls an <b>IQueueCommand</b> method on the Filter Graph Manager, it receives a pointer to the <code>IDeferredCommand</code> interface. The application can use the interface to cancel or postpone the command, or retrieve the return value from the command.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeferredCommand</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDeferredCommand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDeferredCommand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ideferredcommand-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a command that the application previously queued.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ideferredcommand-confidence">Confidence</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ideferredcommand-gethresult">GetHResult</a>
</td>
<td align="left" width="63%">
Retrieves the return value from the invoked command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ideferredcommand-postpone">Postpone</a>
</td>
<td align="left" width="63%">
Specifies a new invocation time for the command.

</td>
</tr>
</table> 

