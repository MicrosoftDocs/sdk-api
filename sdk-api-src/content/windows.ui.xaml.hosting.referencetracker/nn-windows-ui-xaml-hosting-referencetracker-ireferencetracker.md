---
UID: NN:windows.ui.xaml.hosting.referencetracker.IReferenceTracker
title: IReferenceTracker (windows.ui.xaml.hosting.referencetracker.h)
author: windows-sdk-content
description: Defines the interface implemented by the XAML framework for managing XAML object references.
old-location: winrt\ireferencetracker.htm
tech.root: WinRT
ms.assetid: 2267d29f-c3b2-4bc8-b4cb-6272a7ebae1a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IReferenceTracker, IReferenceTracker interface [Windows Runtime], IReferenceTracker interface [Windows Runtime],described, windows/IReferenceTracker, winrt.ireferencetracker
ms.topic: interface
f1_keywords: 
 - "windows.ui.xaml.hosting.referencetracker/IReferenceTracker"
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
 - IReferenceTracker
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IReferenceTracker interface


## -description


Defines the interface implemented by the XAML framework for managing XAML object references.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceTracker</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReferenceTracker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReferenceTracker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-addreffromtrackersource">AddRefFromTrackerSource</a>
</td>
<td align="left" width="63%">
Indicates each time that a tracker source calls <b>IUnknown::AddRef</b> on the reference tracker; called after the <b>AddRef</b> call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-connectfromtrackersource">ConnectFromTrackerSource</a>
</td>
<td align="left" width="63%">
Indicates that a reference tracker source has created its first COM reference on a reference tracker object.  


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-disconnectfromtrackersource">DisconnectFromTrackerSource</a>
</td>
<td align="left" width="63%">
Indicates that a reference tracker source has stopped tracking a reference tracker.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets">FindTrackerTargets</a>
</td>
<td align="left" width="63%">
Finds out what reference tracker targets are reachable from a reference tracker source; must be called by a garbage collector between calls to <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-referencetrackingstarted">ReferenceTrackingStarted</a> and <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-findtrackertargetscompleted">FindTrackerTargetsCompleted</a>.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-getreferencetrackermanager">GetReferenceTrackerManager</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager">IReferenceTrackerManager</a> interface from a XAML object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-pegfromtrackersource">PegFromTrackerSource</a>
</td>
<td align="left" width="63%">
Indicates that a tracker source is unable to protected a reference tracker object.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-releasefromtrackersource">ReleaseFromTrackerSource</a>
</td>
<td align="left" width="63%">
Indicates each time that a tracker source calls <b>IUnknown::Release</b> on the reference tracker; must be called before the <b>Release</b> call.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by most XAML framework objects. It is not defined as <b>agile</b>, nor does it marshal across apartments. Use it only from within the apartment of the XAML object that implements it.



