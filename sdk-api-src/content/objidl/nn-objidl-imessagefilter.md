---
UID: NN:objidl.IMessageFilter
title: IMessageFilter
author: windows-driver-content
description: Provides COM servers and applications with the ability to selectively handle incoming and outgoing COM messages while waiting for responses from synchronous calls.
old-location: com\imessagefilter.htm
old-project: com
ms.assetid: e12d48c0-5033-47a8-bdcd-e94c49857248
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IMessageFilter, IMessageFilter interface [COM], IMessageFilter interface [COM], described, _com_imessagefilter, com.imessagefilter, objidl/IMessageFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IMessageFilter
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMessageFilter interface


## -description


Provides COM servers and applications with the ability to selectively handle incoming and outgoing COM messages while waiting for responses from synchronous calls. Filtering messages helps to ensure that calls are handled in a manner that improves performance and avoids deadlocks. COM messages can be synchronous, asynchronous, or input-synchronized; the majority of interface calls are synchronous.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMessageFilter</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IMessageFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMessageFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e31b518-ef4f-4bdd-b5c7-e1b16383a5be">HandleInComingCall</a>
</td>
<td align="left" width="63%">
Provides a single entry point for incoming calls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4aff53f-c344-4456-b53e-296d5a5b653a">MessagePending</a>
</td>
<td align="left" width="63%">
Indicates that a message has arrived while COM is waiting to respond to a remote call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f800819-2a21-4e46-ad15-f9594fac1a3d">RetryRejectedCall</a>
</td>
<td align="left" width="63%">
Provides applications with an opportunity to display a dialog box offering retry, cancel, or task-switching options.

</td>
</tr>
</table> 


## -remarks



Synchronous calls require the caller to wait for a reply before continuing. COM enters a modal loop while waiting for the reply. During this time, the caller is still able to receive and dispatch incoming messages. 



Asynchronous calls allow the caller to proceed without waiting for a response from the called object. Today, in COM, the only asynchronous calls are to an object's <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface. While the object is processing an asynchronous call, it is prohibited from making any synchronous calls back to the calling object.

To enable behaviors such as focus management and type-ahead to function correctly, input-synchronized calls require the called object to complete the call before relinquishing control. 

<h3><a id="Application_Shutdown_with_WM_QUERYENDSESSION_and_WM_ENDSESSION_"></a><a id="application_shutdown_with_wm_queryendsession_and_wm_endsession_"></a><a id="APPLICATION_SHUTDOWN_WITH_WM_QUERYENDSESSION_AND_WM_ENDSESSION_"></a>Application Shutdown with WM_QUERYENDSESSION and WM_ENDSESSION
</h3>
When a user exits Windows, each open application receives a <a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> message followed by a <a href="https://msdn.microsoft.com/9bf04f24-da1e-4680-a47b-28e9c500635e">WM_ENDSESSION</a> message, provided the exit is not canceled. These messages are invoked with the <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a> function, which unfortunately restricts the initiation of all outgoing LRPC calls. This is a problem for container applications that have open embedded objects when they receive the shutdown request because LRPC is needed to close those objects.

Container and container/server applications with open documents typically display a message box on receipt of the <a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> message that asks if the user wants to save changes before exiting. A positive response is usually the default. The recommendation for dealing with the situation described above is for the application to display an alternate message box asking if the user wants to discard changes; a negative response should be the default. If the user chooses to discard the changes, <b>TRUE</b> should be returned for <b>WM_QUERYENDSESSION</b>, which signals to Windows that it can terminate. If the user does not want to discard the changes, <b>FALSE</b> should be returned. No attempt should be made to close or release running embeddings.

Server applications should return <b>TRUE</b> for <a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> without prompting the user. On receipt of a <a href="https://msdn.microsoft.com/9bf04f24-da1e-4680-a47b-28e9c500635e">WM_ENDSESSION</a> message, all COM applications should execute the normal close sequence for each application's documents and objects. At the same time, you should ignore any errors resulting from any cross-process calls or calls to <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>. All storage pointers (<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> and <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface pointers) must be released to properly flush any temporary files maintained by the compound file implementation of structured storage.




