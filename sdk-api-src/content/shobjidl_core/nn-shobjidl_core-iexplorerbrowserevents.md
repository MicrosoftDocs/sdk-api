---
UID: NN:shobjidl_core.IExplorerBrowserEvents
title: IExplorerBrowserEvents (shobjidl_core.h)
description: Exposes methods for notification of Explorer browser navigation and view creation events.
helpviewer_keywords: ["IExplorerBrowserEvents","IExplorerBrowserEvents interface [Windows Shell]","IExplorerBrowserEvents interface [Windows Shell]","described","_shell_IExplorerBrowserEvents","shell.IExplorerBrowserEvents","shobjidl_core/IExplorerBrowserEvents"]
old-location: shell\IExplorerBrowserEvents.htm
tech.root: shell
ms.assetid: 802d547f-41c2-4c4a-9f07-be615d7b86eb
ms.date: 12/05/2018
ms.keywords: IExplorerBrowserEvents, IExplorerBrowserEvents interface [Windows Shell], IExplorerBrowserEvents interface [Windows Shell],described, _shell_IExplorerBrowserEvents, shell.IExplorerBrowserEvents, shobjidl_core/IExplorerBrowserEvents
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
 - IExplorerBrowserEvents
 - shobjidl_core/IExplorerBrowserEvents
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
 - IExplorerBrowserEvents
---

# IExplorerBrowserEvents interface


## -description

Exposes methods for notification of Explorer browser navigation and view creation events.

## -inheritance

The <b>IExplorerBrowserEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExplorerBrowserEvents</b> also has these types of members:

## -remarks

Implement this interface to be notified of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a> navigation and view creation events; implementation enables handling of these events, if desired.


<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a> must be notified of implementers (clients) who want to be advised of <b>IExplorerBrowser</b> events. Clients do this by calling the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-advise">IExplorerBrowser::Advise</a> method. This enables event callbacks by <b>IExplorerBrowser</b> to the client using the methods in <b>IExplorerBrowserEvents</b>. To stop event callbacks, the client must call method <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-unadvise">IExplorerBrowser::Unadvise</a> or a memory leak may result.

During its first navigation (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-browsetoobject">IExplorerBrowser::BrowseToObject</a>), Explorer calls the methods in this interface synchronously. After that, Explorer calls them asynchronously. The order of the event callbacks is as follows: <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationpending">IExplorerBrowserEvents::OnNavigationPending</a>; <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onviewcreated">IExplorerBrowserEvents::OnViewCreated</a>;
and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationcomplete">IExplorerBrowserEvents::OnNavigationComplete</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationfailed">IExplorerBrowserEvents::OnNavigationFailed</a> depending on whether the navigation succeeded or failed.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a>
