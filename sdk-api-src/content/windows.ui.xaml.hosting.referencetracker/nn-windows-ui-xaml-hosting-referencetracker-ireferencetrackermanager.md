---
UID: NN:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerManager
title: IReferenceTrackerManager (windows.ui.xaml.hosting.referencetracker.h)
description: Defines the interface for a XAML object reference manager. Implement this interface to manage instances of IReferenceTracker on XAML objects.
helpviewer_keywords: ["IReferenceTrackerManager","IReferenceTrackerManager interface [Windows Runtime]","IReferenceTrackerManager interface [Windows Runtime]","described","windows/IReferenceTrackerManager","winrt.ireferencetrackermanager"]
old-location: winrt\ireferencetrackermanager.htm
tech.root: WinRT
ms.assetid: bdac39a0-a51a-49cc-b554-58450c722a46
ms.date: 12/05/2018
ms.keywords: IReferenceTrackerManager, IReferenceTrackerManager interface [Windows Runtime], IReferenceTrackerManager interface [Windows Runtime],described, windows/IReferenceTrackerManager, winrt.ireferencetrackermanager
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IReferenceTrackerManager
 - windows.ui.xaml.hosting.referencetracker/IReferenceTrackerManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.ui.xaml.hosting.referencetracker.h
api_name:
 - IReferenceTrackerManager
---

# IReferenceTrackerManager interface


## -description

Defines the interface for  a XAML object reference manager. Implement this interface to manage instances of <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker">IReferenceTracker</a> on XAML objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceTrackerManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReferenceTrackerManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReferenceTrackerManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-findtrackertargetscompleted">FindTrackerTargetsCompleted</a>
</td>
<td align="left" width="63%">
Indicates that a garbage collection system has finished making all the calls it needs to <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets">IReferenceTracker::FindTrackerTargets</a>;   by this time, XAML has pegged all reference tracker targets that it wants to protect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-referencetrackingcompleted">ReferenceTrackingCompleted</a>
</td>
<td align="left" width="63%">
Indicates that a garbage collection system has finished with its collection process;  at this point, XAML unblocks threads attempting to update tracked references.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-referencetrackingstarted">ReferenceTrackingStarted</a>
</td>
<td align="left" width="63%">
Indicates that a garbage collector is performing a collection; when the collection is finished, the garbage collector calls <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-findtrackertargetscompleted">FindTrackerTargetsCompleted</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-setreferencetrackerhost">SetReferenceTrackerHost</a>
</td>
<td align="left" width="63%">
Registers an <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost">IReferenceTrackerHost</a> interface with XAML.

</td>
</tr>
</table>

## -remarks

Obtain a reference to an implementation of this interface by calling <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-getreferencetrackermanager">IReferenceTracker::GetReferenceTrackerManager</a> on a XAML object that implements <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker">IReferenceTracker</a>.

There is only one instance of <b>IReferenceTrackerManager</b> for a process, and it may be called from any thread.