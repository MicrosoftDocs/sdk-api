---
UID: NF:shobjidl_core.IExplorerBrowser.Advise
title: IExplorerBrowser::Advise (shobjidl_core.h)
description: Initiates a connection with IExplorerBrowser for event callbacks.
helpviewer_keywords: ["Advise","Advise method [Windows Shell]","Advise method [Windows Shell]","IExplorerBrowser interface","IExplorerBrowser interface [Windows Shell]","Advise method","IExplorerBrowser.Advise","IExplorerBrowser::Advise","_shell_IExplorerBrowser_Advise","shell.IExplorerBrowser_Advise","shobjidl_core/IExplorerBrowser::Advise"]
old-location: shell\IExplorerBrowser_Advise.htm
tech.root: shell
ms.assetid: b77f9c41-248e-4f16-a9ff-6ff5437df11c
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],Advise method, IExplorerBrowser.Advise, IExplorerBrowser::Advise, _shell_IExplorerBrowser_Advise, shell.IExplorerBrowser_Advise, shobjidl_core/IExplorerBrowser::Advise
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IExplorerBrowser::Advise
 - shobjidl_core/IExplorerBrowser::Advise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerBrowser.Advise
---

# IExplorerBrowser::Advise


## -description

Initiates a connection with <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a> for event callbacks.

## -parameters

### -param psbe [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowserevents">IExplorerBrowserEvents</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowserevents">IExplorerBrowserEvents</a> interface of the object to be advised of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a> events.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

When this method returns, contains a token that uniquely identifies the event listener.  This allows several event listeners to be subscribed at a time.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by an implementer of  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowserevents">IExplorerBrowserEvents</a>. The implementer (listener) is advised of ExplorerBrowser view and navigation events by callback of the methods of <b>IExplorerBrowserEvents</b>.

Call <b>IExplorerBrowser::Advise</b> to initiate an advisory connection prior to the first <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a> navigation.  Callbacks to event listeners are made as the browser is browsing.

The first browse happens synchronously to a call on <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-browsetoobject">IExplorerBrowser::BrowseToObject</a>, or a similar method. Future callbacks happen asynchronously, as the browser browses.

When the connection is no longer needed, call method <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-unadvise">IExplorerBrowser::Unadvise</a> to terminate the connection.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationcomplete">OnNavigationComplete</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationfailed">OnNavigationFailed</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onviewcreated">OnViewCreated</a>