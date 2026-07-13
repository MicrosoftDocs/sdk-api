---
UID: NF:messagedispatcherapi.CoSetMessageDispatcher
title: CoSetMessageDispatcher function (messagedispatcherapi.h)
description: Registers or unregisters the per-thread message dispatcher that is to be invoked when there are window messages available to dispatch within COM wait APIs on an ASTA thread.
helpviewer_keywords: ["CoSetMessageDispatcher","CoSetMessageDispatcher function [COM]","com.cosetmessagedispatcher","messagedispatcherapi/CoSetMessageDispatcher"]
old-location: com\cosetmessagedispatcher.htm
tech.root: com
ms.assetid: 3D6CFE01-8D3D-474E-A7D0-9B129ECD4EEA
ms.date: 12/05/2018
ms.keywords: CoSetMessageDispatcher, CoSetMessageDispatcher function [COM], com.cosetmessagedispatcher, messagedispatcherapi/CoSetMessageDispatcher
req.header: messagedispatcherapi.h
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
req.lib: Ole32.Lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoSetMessageDispatcher
 - messagedispatcherapi/CoSetMessageDispatcher
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - messagedispatcherapi.h
api_name:
 - CoSetMessageDispatcher
---

# CoSetMessageDispatcher function


## -description

Registers or unregisters the per-thread message dispatcher that is to be invoked when there are window messages available to dispatch within COM wait APIs on an ASTA thread. This function is usually called by CoreWindow, but in certain circumstances other components that need to specialize how messages are dispatched on an ASTA thread can also call this function.

## -parameters

### -param pMessageDispatcher [in, optional]

If non-null, message dispatcher object to register. This object must also implement <a href="/windows/desktop/api/weakreference/nn-weakreference-iweakreferencesource">IWeakReferenceSource</a>. If null, unregisters the current message dispatcher.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is supported only in ASTA threads. An attempt to set the message dispatcher on a non-ASTA thread silently fails with no side effects.



An attempt to set an object that does not implement <a href="/windows/desktop/api/weakreference/nn-weakreference-iweakreferencesource">IWeakReferenceSource</a> silently fails with no side effects.



A call to this function with a valid and non-null <i>pMessageDispatcher</i> parameter registers this object to receive a <a href="/windows/desktop/api/imessagedispatcher/nf-imessagedispatcher-imessagedispatcher-pumpmessages">PumpMessages</a> callback whenever there are window messages available to dispatch with COM wait APIs on that ASTA thread. A Windows Runtime weak reference to this object is held, and the object receives callbacks, until the registration is replaced or the ASTA uninitialized. Each call to this function replaces the previously registered message dispatcher, if any.



There is no way to check if a message dispatcher is registered on an ASTA thread or to retrieve a previously registered message dispatcher. This function should only be called under circumstances where it is known that this will not collide with another registration, specifically:


<ul>
<li>In Windows Store app UI threads, this function is called by CoreWindow to register its dispatcher. No other components should call this function on these threads.
</li>
<li>UI frameworks may support an authoring mode, in which applications are run in the desktop environment and therefore do not have a CoreWindow in their UI threads. In lieu of CoreWindow support, these UI frameworks may register a message dispatcher on UI threads to handle special window message processing usually handled by CoreWindow (such as accelerators). It is not required to call this function if the UI framework has no need for this functionality.
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility">IAppVisibility</a> browsers are not restricted to the Windows Store app APIs and therefore may have their own custom window message processing using user32 APIs. However, these applications still have ASTA UI threads as provided by app object, and may register a message dispatcher to handle this special processing. It is not required to call this function if the browser has no need for this functionality.

</li>
</ul>
The case of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility">IAppVisibility</a> browsers requires care to avoid CoreWindow replacing the browser’s message dispatcher. It is assumed that the browser has no need for CoreWindow’s dispatcher. The browser should call <b>CoSetMessageDispatcher</b> no sooner than its IViewProvider::Initialize, or, in the case of views that implement IInitializeWithWindowFactory, no sooner than after it has created a window on the thread.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility">IAppVisibility</a>