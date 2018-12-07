---
UID: NN:imessagedispatcher.IMessageDispatcher
title: IMessageDispatcher
author: windows-sdk-content
description: Callback interface implemented by components that need to perform special processing of window messages on an ASTA thread.
old-location: com\imessagedispatcher.htm
tech.root: com
ms.assetid: 60FD9084-CC79-48FE-AB26-C8FCB4288851
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMessageDispatcher, IMessageDispatcher interface [COM], IMessageDispatcher interface [COM],described, com.imessagedispatcher, imessagedispatcher/IMessageDispatcher
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: imessagedispatcher.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imessagedispatcher.h
api_name:
 - IMessageDispatcher
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMessageDispatcher interface


## -description


Callback interface implemented by components that need to perform special processing of window messages on an ASTA thread.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMessageDispatcher</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IMessageDispatcher</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMessageDispatcher</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CC34B3B0-C956-4B37-8DF7-CC90A0160835">PumpMessages</a>
</td>
<td align="left" width="63%">
Performs custom dispatching when window messages are available to be dispatched on an ASTA thread.

</td>
</tr>
</table> 

