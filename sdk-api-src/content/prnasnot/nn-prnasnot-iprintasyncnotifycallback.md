---
UID: NN:prnasnot.IPrintAsyncNotifyCallback
title: IPrintAsyncNotifyCallback
author: windows-sdk-content
description: Creates and manages a communication channel used by applications and components that are hosted by the print spooler.
old-location: gdi\iprintasyncnotifycallback.htm
tech.root: printdocs
ms.assetid: e2b021cd-1cfd-42b7-b6e4-7f8671b013f6
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IPrintAsyncNotifyCallback, IPrintAsyncNotifyCallback interface [Windows GDI], IPrintAsyncNotifyCallback interface [Windows GDI],described, _win32_IPrintAsyncNotifyCallback, gdi.iprintasyncnotifycallback, prnasnot/IPrintAsyncNotifyCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: prnasnot.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.h
api_name:
 - IPrintAsyncNotifyCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrintAsyncNotifyCallback interface


## -description


Creates and manages a communication channel used by applications and components that are hosted by the print spooler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintAsyncNotifyCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPrintAsyncNotifyCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrintAsyncNotifyCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/245f4d86-a6b9-421a-add5-fb7afbbacb45">ChannelClosed</a>
</td>
<td align="left" width="63%">
Used by one member of a communication channel to advise the other member that the channel is being closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f398173-3cd6-46da-931d-057d1dccbe9b">OnEventNotify</a>
</td>
<td align="left" width="63%">
Used by a notification sender to alert a listener that a notification is available on a specified channel. It is also used for responses to notifications.

</td>
</tr>
</table> 


## -remarks



For an application to receive notifications from a Print Spooler-hosted component, it must provide an <b>IPrintAsyncNotifyCallback</b> object when it registers for notifications.

A Print Spooler-hosted component that opens a bidirectional communication channel with a listening application must provide an <b>IPrintAsyncNotifyCallback</b> object.




## -see-also




<a href="https://msdn.microsoft.com/e96c957f-3972-4afc-9d76-a4725b8688f8">Asynchronous Printing Notification Interfaces</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

