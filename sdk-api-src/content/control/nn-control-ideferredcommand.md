---
UID: NN:control.IDeferredCommand
title: IDeferredCommand
author: windows-sdk-content
description: The IDeferredCommand interface cancels or modify graph-control commands that were queued using the IQueueCommand interface.When an application calls an IQueueCommand method on the Filter Graph Manager, it receives a pointer to the IDeferredCommand interface. The application can use the interface to cancel or postpone the command, or retrieve the return value from the command.
old-location: dshow\ideferredcommand.htm
tech.root: DirectShow
ms.assetid: 8161932a-16aa-4700-b91d-b4d8948ad59f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDeferredCommand, IDeferredCommand interface [DirectShow], IDeferredCommand interface [DirectShow],described, IDeferredCommandInterface, control/IDeferredCommand, dshow.ideferredcommand
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
 - IDeferredCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeferredCommand interface


## -description



The <code>IDeferredCommand</code> interface cancels or modify graph-control commands that were queued using the <a href="https://msdn.microsoft.com/en-us/library/Dd376922(v=VS.85).aspx">IQueueCommand</a> interface.

When an application calls an <b>IQueueCommand</b> method on the Filter Graph Manager, it receives a pointer to the <code>IDeferredCommand</code> interface. The application can use the interface to cancel or postpone the command, or retrieve the return value from the command.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeferredCommand</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IDeferredCommand</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd406763(v=VS.85).aspx">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a command that the application previously queued.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406764(v=VS.85).aspx">Confidence</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406765(v=VS.85).aspx">GetHResult</a>
</td>
<td align="left" width="63%">
Retrieves the return value from the invoked command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406766(v=VS.85).aspx">Postpone</a>
</td>
<td align="left" width="63%">
Specifies a new invocation time for the command.

</td>
</tr>
</table> 

