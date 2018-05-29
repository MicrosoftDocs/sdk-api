---
UID: NN:shobjidl_core.IExplorerBrowserEvents
title: IExplorerBrowserEvents
author: windows-sdk-content
description: Exposes methods for notification of Explorer browser navigation and view creation events.
old-location: shell\IExplorerBrowserEvents.htm
old-project: shell
ms.assetid: 802d547f-41c2-4c4a-9f07-be615d7b86eb
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IExplorerBrowserEvents, IExplorerBrowserEvents interface [Windows Shell], IExplorerBrowserEvents interface [Windows Shell],described, _shell_IExplorerBrowserEvents, shell.IExplorerBrowserEvents, shobjidl_core/IExplorerBrowserEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IExplorerBrowserEvents
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IExplorerBrowserEvents interface


## -description


Exposes methods for notification of Explorer browser navigation and view creation events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExplorerBrowserEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExplorerBrowserEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/54c97a55-a8d1-4635-a1e0-2f92d52ddc10">OnNavigationComplete</a>
</td>
<td align="left" width="63%">
Notifies clients that the Explorer browser has successfully navigated to a Shell folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4de3b81-4482-47c8-bb47-593aba484952">OnNavigationFailed</a>
</td>
<td align="left" width="63%">
Notifies clients that the Explorer browser has failed to navigate to a Shell folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52dfb901-ee65-444a-8b27-2d2811cf83c0">OnNavigationPending</a>
</td>
<td align="left" width="63%">
Notifies clients of a pending Explorer browser navigation to a Shell folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/801d59f5-6e92-4e3c-938a-e94b43b7c6f1">OnViewCreated</a>
</td>
<td align="left" width="63%">
Notifies clients that the view of the Explorer browser has been created and can be modified.

</td>
</tr>
</table> 


## -remarks



Implement this interface to be notified of <a href="https://msdn.microsoft.com/da2cf5d4-5a68-4d18-807b-b9d4e2712c10">IExplorerBrowser</a> navigation and view creation events; implementation enables handling of these events, if desired.


<a href="https://msdn.microsoft.com/da2cf5d4-5a68-4d18-807b-b9d4e2712c10">IExplorerBrowser</a> must be notified of implementers (clients) who want to be advised of <b>IExplorerBrowser</b> events. Clients do this by calling the <a href="https://msdn.microsoft.com/b77f9c41-248e-4f16-a9ff-6ff5437df11c">IExplorerBrowser::Advise</a> method. This enables event callbacks by <b>IExplorerBrowser</b> to the client using the methods in <b>IExplorerBrowserEvents</b>. To stop event callbacks, the client must call method <a href="https://msdn.microsoft.com/a9b6b971-5676-4ceb-ab48-2350a1715b82">IExplorerBrowser::Unadvise</a> or a memory leak may result.

During its first navigation (<a href="https://msdn.microsoft.com/cbfe2348-9fdc-4839-bf8b-b2a65caefa4c">IExplorerBrowser::BrowseToObject</a>), Explorer calls the methods in this interface synchronously. After that, Explorer calls them asynchronously. The order of the event callbacks is as follows: <a href="https://msdn.microsoft.com/52dfb901-ee65-444a-8b27-2d2811cf83c0">IExplorerBrowserEvents::OnNavigationPending</a>; <a href="https://msdn.microsoft.com/801d59f5-6e92-4e3c-938a-e94b43b7c6f1">IExplorerBrowserEvents::OnViewCreated</a>;
and <a href="https://msdn.microsoft.com/54c97a55-a8d1-4635-a1e0-2f92d52ddc10">IExplorerBrowserEvents::OnNavigationComplete</a> or <a href="https://msdn.microsoft.com/d4de3b81-4482-47c8-bb47-593aba484952">IExplorerBrowserEvents::OnNavigationFailed</a> depending on whether the navigation succeeded or failed.




## -see-also




<a href="https://msdn.microsoft.com/da2cf5d4-5a68-4d18-807b-b9d4e2712c10">IExplorerBrowser</a>
 

 

