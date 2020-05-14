---
UID: NN:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerTarget
title: IReferenceTrackerTarget (windows.ui.xaml.hosting.referencetracker.h)
description: Defines an interface implemented by a garbage collector object referenced from XAML.helpviewer_keywords: ["IReferenceTrackerTarget","IReferenceTrackerTarget interface [Windows Runtime]","IReferenceTrackerTarget interface [Windows Runtime]","described","windows/IReferenceTrackerTarget","winrt.ireferencetrackertarget"]
old-location: winrt\ireferencetrackertarget.htm
tech.root: WinRT
ms.assetid: 204c647d-65c0-4b0e-b0fa-1abe9e8fdedd
ms.date: 12/05/2018
ms.keywords: IReferenceTrackerTarget, IReferenceTrackerTarget interface [Windows Runtime], IReferenceTrackerTarget interface [Windows Runtime],described, windows/IReferenceTrackerTarget, winrt.ireferencetrackertarget
f1_keywords:
- windows.ui.xaml.hosting.referencetracker/IReferenceTrackerTarget
dev_langs:
- c++
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
- IReferenceTrackerTarget
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IReferenceTrackerTarget interface


## -description


Defines an interface implemented by a garbage collector object referenced from XAML.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceTrackerTarget</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReferenceTrackerTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReferenceTrackerTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget-addreffromreferencetracker">AddRefFromReferenceTracker</a>
</td>
<td align="left" width="63%">
Indicates that the reference tracker is returning the target XAML object(s) from previous calls to  <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets">FindTrackerTargets</a>.  Note that the reference is held by the reference tracker object in lieu of <b>IUnknown::AddRef</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget-peg">Peg</a>
</td>
<td align="left" width="63%">
Marks that the reference tracker target is in use by the XAML framework, and should not be collected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget-releasefromreferencetracker">ReleaseFromReferenceTracker</a>
</td>
<td align="left" width="63%">
Releases the XAML object reference marked in a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget-addreffromreferencetracker">AddRefFromReferenceTracker</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget-unpeg">Unpeg</a>
</td>
<td align="left" width="63%">
Marks that the reference tracker target is no longer in use by the XAML framework, and can be collected.  

</td>
</tr>
</table> 

