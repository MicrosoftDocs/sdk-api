---
UID: NN:objidl.IMessageFilter
title: IMessageFilter (objidl.h)
description: Provides COM servers and applications with the ability to selectively handle incoming and outgoing COM messages while waiting for responses from synchronous calls.
helpviewer_keywords: ["IMessageFilter","IMessageFilter interface [COM]","IMessageFilter interface [COM]","described","_com_imessagefilter","com.imessagefilter","objidl/IMessageFilter"]
old-location: com\imessagefilter.htm
tech.root: com
ms.assetid: e12d48c0-5033-47a8-bdcd-e94c49857248
ms.date: 12/05/2018
ms.keywords: IMessageFilter, IMessageFilter interface [COM], IMessageFilter interface [COM],described, _com_imessagefilter, com.imessagefilter, objidl/IMessageFilter
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMessageFilter
 - objidl/IMessageFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IMessageFilter
---

# IMessageFilter interface


## -description

Provides COM servers and applications with the ability to selectively handle incoming and outgoing COM messages while waiting for responses from synchronous calls. Filtering messages helps to ensure that calls are handled in a manner that improves performance and avoids deadlocks. COM messages can be synchronous, asynchronous, or input-synchronized; the majority of interface calls are synchronous.

## -inheritance

The <b>IMessageFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMessageFilter</b> also has these types of members:

## -remarks

Synchronous calls require the caller to wait for a reply before continuing. COM enters a modal loop while waiting for the reply. During this time, the caller is still able to receive and dispatch incoming messages. 



Asynchronous calls allow the caller to proceed without waiting for a response from the called object. Today, in COM, the only asynchronous calls are to an object's <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface. While the object is processing an asynchronous call, it is prohibited from making any synchronous calls back to the calling object.

To enable behaviors such as focus management and type-ahead to function correctly, input-synchronized calls require the called object to complete the call before relinquishing control. 

<h3><a id="Application_Shutdown_with_WM_QUERYENDSESSION_and_WM_ENDSESSION_"></a><a id="application_shutdown_with_wm_queryendsession_and_wm_endsession_"></a><a id="APPLICATION_SHUTDOWN_WITH_WM_QUERYENDSESSION_AND_WM_ENDSESSION_"></a>Application Shutdown with WM_QUERYENDSESSION and WM_ENDSESSION
</h3>
When a user exits Windows, each open application receives a <a href="/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> message followed by a <a href="/windows/desktop/Shutdown/wm-endsession">WM_ENDSESSION</a> message, provided the exit is not canceled. These messages are invoked with the <a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a> function, which unfortunately restricts the initiation of all outgoing LRPC calls. This is a problem for container applications that have open embedded objects when they receive the shutdown request because LRPC is needed to close those objects.

Container and container/server applications with open documents typically display a message box on receipt of the <a href="/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> message that asks if the user wants to save changes before exiting. A positive response is usually the default. The recommendation for dealing with the situation described above is for the application to display an alternate message box asking if the user wants to discard changes; a negative response should be the default. If the user chooses to discard the changes, <b>TRUE</b> should be returned for <b>WM_QUERYENDSESSION</b>, which signals to Windows that it can terminate. If the user does not want to discard the changes, <b>FALSE</b> should be returned. No attempt should be made to close or release running embeddings.

Server applications should return <b>TRUE</b> for <a href="/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> without prompting the user. On receipt of a <a href="/windows/desktop/Shutdown/wm-endsession">WM_ENDSESSION</a> message, all COM applications should execute the normal close sequence for each application's documents and objects. At the same time, you should ignore any errors resulting from any cross-process calls or calls to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>. All storage pointers (<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> and <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface pointers) must be released to properly flush any temporary files maintained by the compound file implementation of structured storage.
