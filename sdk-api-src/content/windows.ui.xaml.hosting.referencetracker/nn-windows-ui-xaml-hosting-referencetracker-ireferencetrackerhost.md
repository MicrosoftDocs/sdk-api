---
UID: NN:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost
title: IReferenceTrackerHost (windows.ui.xaml.hosting.referencetracker.h)
author: windows-sdk-content
description: Defines an interface that provides the global services used by the garbage collection (GC) system used by the XAML framework.
old-location: winrt\ireferencetrackerhost.htm
tech.root: WinRT
ms.assetid: b17fe8ae-be79-4281-a313-517505017401
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IReferenceTrackerHost, IReferenceTrackerHost interface [Windows Runtime], IReferenceTrackerHost interface [Windows Runtime],described, windows/IReferenceTrackerHost, winrt.ireferencetrackerhost
ms.topic: interface
f1_keywords: ["windows.ui.xaml.hosting.referencetracker/IReferenceTrackerHost"]
req.header: windows.ui.xaml.hosting.referencetracker.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.ui.xaml.hosting.referencetracker.idl
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
 - Windows.ui.xaml.hosting.referencetracker.h
api_name:
 - IReferenceTrackerHost
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IReferenceTrackerHost interface


## -description


Defines an interface that provides the global services used by the garbage collection (GC) system used by the XAML framework.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceTrackerHost</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReferenceTrackerHost</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReferenceTrackerHost</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost-addmemorypressure">AddMemoryPressure</a>
</td>
<td align="left" width="63%">
Informs the host of increased memory allocations since the last notification.
The CLR uses this to inform the algorithm that determines when to run a garbage collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost-disconnectunusedreferencesources">DisconnectUnusedReferenceSources</a>
</td>
<td align="left" width="63%">
Requests that the host perform a garbage collection and remove all unnecessary reference sources.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost-gettrackertarget">GetTrackerTarget</a>
</td>
<td align="left" width="63%">
Requests the host to provide a reference tracker target that references a reference tracker source. This tracker target then controls the lifetime of the tracker source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost-notifyendofreferencetrackingonthread">NotifyEndOfReferenceTrackingOnThread</a>
</td>
<td align="left" width="63%">
Notifies the host that reference tracking is no longer available on the calling thread; XAML calls this when the <b>FrameworkView</b> is uninitialized.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost-releasedisconnectedreferencesources">ReleaseDisconnectedReferenceSources</a>
</td>
<td align="left" width="63%">
Requests that the host call <b>IUnknown::Release</b> on any reference tracker objects that have been disconnected by a reference source.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost-removememorypressure">RemoveMemoryPressure</a>
</td>
<td align="left" width="63%">
Informs the host of reduced memory allocations since the last notification.

</td>
</tr>
</table> 


## -remarks



An implementation of this interface must be registered with the XAML framework by passing it to the <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-setreferencetrackerhost">IReferenceTrackerManager::SetReferenceTrackerHost</a> method.



