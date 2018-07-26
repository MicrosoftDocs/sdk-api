---
UID: NN:prnasnot.IPrintAsyncNotifyChannel
title: IPrintAsyncNotifyChannel
author: windows-sdk-content
description: Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications. If the channel is bidirectional, applications can use the same channel to send responses back to the component.
old-location: gdi\iprintasyncnotifychannel.htm
old-project: printdocs
ms.assetid: 8973cf5a-bbce-43c2-b418-2807842d43c0
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IPrintAsyncNotifyChannel, IPrintAsyncNotifyChannel interface [Windows GDI], IPrintAsyncNotifyChannel interface [Windows GDI],described, _win32_IPrintAsyncNotifyChannel, gdi.iprintasyncnotifychannel, prnasnot/IPrintAsyncNotifyChannel
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PrintAsyncNotifyUserFilter
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.h
api_name:
 - IPrintAsyncNotifyChannel
product: Windows
targetos: Windows
req.lib: WinSpool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: ADAM
---

# IPrintAsyncNotifyChannel interface


## -description


Represents a communication channel that  components that are hosted by the print spooler use to send notifications to applications. If the channel is bidirectional, applications can use the same channel to send responses back to the component.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintAsyncNotifyChannel</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPrintAsyncNotifyChannel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrintAsyncNotifyChannel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5878cf1-c2c3-4f33-bc08-e4f868c8a5e7">CloseChannel</a>
</td>
<td align="left" width="63%">
Closes the channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/729286d4-75ee-441e-b63d-fef72d41533a">SendNotification</a>
</td>
<td align="left" width="63%">
Sends a notification from a Print Spooler-hosted component to one or more listening applications, or sends a response from an application back to a component.

</td>
</tr>
</table> 


## -remarks



Objects implementing this interface are created by the Print Spooler in response to a call of <a href="https://msdn.microsoft.com/52cc586a-a565-46c6-b1b7-8613ad111ed3">CreatePrintAsyncNotifyChannel</a> by a Print Spooler-hosted component.

Call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IPrintAsyncNotifyChannel::Release</a> only:

<ol>
<li>if it is an explicit match to an earlier <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IPrintAsyncNotifyChannel::AddRef</a> call.</li>
<li>if the channel is a UniDirectional channel and you are abandoning the pointer received in a successful call to <a href="https://msdn.microsoft.com/52cc586a-a565-46c6-b1b7-8613ad111ed3">CreatePrintAsyncNotifyChannel</a>.</li>
<li>if, after you created a BiDirectional channel or in the implementation of <a href="https://msdn.microsoft.com/2f398173-3cd6-46da-931d-057d1dccbe9b">IPrintAsyncNotifyCallback::OnEventNotify</a> and:<ol>
<li>you did not call <a href="https://msdn.microsoft.com/729286d4-75ee-441e-b63d-fef72d41533a">IPrintAsyncNotifyChannel::SendNotification</a> or <a href="https://msdn.microsoft.com/d5878cf1-c2c3-4f33-bc08-e4f868c8a5e7">IPrintAsyncNotifyChannel::CloseChannel</a> OR</li>
<li>you did not retry a call to <a href="https://msdn.microsoft.com/729286d4-75ee-441e-b63d-fef72d41533a">IPrintAsyncNotifyChannel::SendNotification</a> or <a href="https://msdn.microsoft.com/d5878cf1-c2c3-4f33-bc08-e4f868c8a5e7">IPrintAsyncNotifyChannel::CloseChannel</a> that failed OR</li>
<li>on the server side, you did not retry a call to <a href="https://msdn.microsoft.com/729286d4-75ee-441e-b63d-fef72d41533a">IPrintAsyncNotifyChannel::SendNotification</a> that succeeded with the return value NO_LISTENER OR</li>
<li>on the client side, you did not retry a call to <a href="https://msdn.microsoft.com/729286d4-75ee-441e-b63d-fef72d41533a">IPrintAsyncNotifyChannel::SendNotification</a> that succeeded with return value CHANNEL_ACQUIRED.</li>
</ol>
</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/e96c957f-3972-4afc-9d76-a4725b8688f8">Asynchronous Printing Notification Interfaces</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

