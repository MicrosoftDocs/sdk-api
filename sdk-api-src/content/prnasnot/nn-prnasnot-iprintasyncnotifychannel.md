---
UID: NN:prnasnot.IPrintAsyncNotifyChannel
title: IPrintAsyncNotifyChannel (prnasnot.h)
description: Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications. If the channel is bidirectional, applications can use the same channel to send responses back to the component.
helpviewer_keywords: ["IPrintAsyncNotifyChannel","IPrintAsyncNotifyChannel interface [Windows GDI]","IPrintAsyncNotifyChannel interface [Windows GDI]","described","_win32_IPrintAsyncNotifyChannel","gdi.iprintasyncnotifychannel","prnasnot/IPrintAsyncNotifyChannel"]
old-location: gdi\iprintasyncnotifychannel.htm
tech.root: xps
ms.assetid: 8973cf5a-bbce-43c2-b418-2807842d43c0
ms.date: 12/05/2018
ms.keywords: IPrintAsyncNotifyChannel, IPrintAsyncNotifyChannel interface [Windows GDI], IPrintAsyncNotifyChannel interface [Windows GDI],described, _win32_IPrintAsyncNotifyChannel, gdi.iprintasyncnotifychannel, prnasnot/IPrintAsyncNotifyChannel
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPrintAsyncNotifyChannel
 - prnasnot/IPrintAsyncNotifyChannel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.h
api_name:
 - IPrintAsyncNotifyChannel
---

# IPrintAsyncNotifyChannel interface


## -description

Represents a communication channel that  components that are hosted by the print spooler use to send notifications to applications. If the channel is bidirectional, applications can use the same channel to send responses back to the component.

## -inheritance

The <b>IPrintAsyncNotifyChannel</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPrintAsyncNotifyChannel</b> also has these types of members:

## -remarks

Objects implementing this interface are created by the Print Spooler in response to a call of <a href="/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel">CreatePrintAsyncNotifyChannel</a> by a Print Spooler-hosted component.

Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IPrintAsyncNotifyChannel::Release</a> only:

<ol>
<li>if it is an explicit match to an earlier <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IPrintAsyncNotifyChannel::AddRef</a> call.</li>
<li>if the channel is a UniDirectional channel and you are abandoning the pointer received in a successful call to <a href="/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel">CreatePrintAsyncNotifyChannel</a>.</li>
<li>if, after you created a BiDirectional channel or in the implementation of <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-oneventnotify">IPrintAsyncNotifyCallback::OnEventNotify</a> and:<ol>
<li>you did not call <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification">IPrintAsyncNotifyChannel::SendNotification</a> or <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel">IPrintAsyncNotifyChannel::CloseChannel</a> OR</li>
<li>you did not retry a call to <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification">IPrintAsyncNotifyChannel::SendNotification</a> or <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel">IPrintAsyncNotifyChannel::CloseChannel</a> that failed OR</li>
<li>on the server side, you did not retry a call to <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification">IPrintAsyncNotifyChannel::SendNotification</a> that succeeded with the return value NO_LISTENER OR</li>
<li>on the client side, you did not retry a call to <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification">IPrintAsyncNotifyChannel::SendNotification</a> that succeeded with return value CHANNEL_ACQUIRED.</li>
</ol>
</li>
</ol>

## -see-also

<a href="/windows/desktop/printdocs/asynchronous-notification-interfaces">Asynchronous Printing Notification Interfaces</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>
