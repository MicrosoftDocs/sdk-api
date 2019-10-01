---
UID: NN:shobjidl_core.IExplorerBrowserEvents
title: IExplorerBrowserEvents (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods for notification of Explorer browser navigation and view creation events.
old-location: shell\IExplorerBrowserEvents.htm
tech.root: shell
ms.assetid: 802d547f-41c2-4c4a-9f07-be615d7b86eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IExplorerBrowserEvents, IExplorerBrowserEvents interface [Windows Shell], IExplorerBrowserEvents interface [Windows Shell],described, _shell_IExplorerBrowserEvents, shell.IExplorerBrowserEvents, shobjidl_core/IExplorerBrowserEvents
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IExplorerBrowserEvents"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerBrowserEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExplorerBrowserEvents interface


## -description


Exposes methods for notification of Explorer browser navigation and view creation events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExplorerBrowserEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExplorerBrowserEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExplorerBrowserEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationcomplete">OnNavigationComplete</a>
</td>
<td align="left" width="63%">
Notifies clients that the Explorer browser has successfully navigated to a Shell folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationfailed">OnNavigationFailed</a>
</td>
<td align="left" width="63%">
Notifies clients that the Explorer browser has failed to navigate to a Shell folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationpending">OnNavigationPending</a>
</td>
<td align="left" width="63%">
Notifies clients of a pending Explorer browser navigation to a Shell folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onviewcreated">OnViewCreated</a>
</td>
<td align="left" width="63%">
Notifies clients that the view of the Explorer browser has been created and can be modified.

</td>
</tr>
</table> 


## -remarks



Implement this interface to be notified of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a> navigation and view creation events; implementation enables handling of these events, if desired.


<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a> must be notified of implementers (clients) who want to be advised of <b>IExplorerBrowser</b> events. Clients do this by calling the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-advise">IExplorerBrowser::Advise</a> method. This enables event callbacks by <b>IExplorerBrowser</b> to the client using the methods in <b>IExplorerBrowserEvents</b>. To stop event callbacks, the client must call method <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-unadvise">IExplorerBrowser::Unadvise</a> or a memory leak may result.

During its first navigation (<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-browsetoobject">IExplorerBrowser::BrowseToObject</a>), Explorer calls the methods in this interface synchronously. After that, Explorer calls them asynchronously. The order of the event callbacks is as follows: <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationpending">IExplorerBrowserEvents::OnNavigationPending</a>; <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onviewcreated">IExplorerBrowserEvents::OnViewCreated</a>;
and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationcomplete">IExplorerBrowserEvents::OnNavigationComplete</a> or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowserevents-onnavigationfailed">IExplorerBrowserEvents::OnNavigationFailed</a> depending on whether the navigation succeeded or failed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a>
 

 

