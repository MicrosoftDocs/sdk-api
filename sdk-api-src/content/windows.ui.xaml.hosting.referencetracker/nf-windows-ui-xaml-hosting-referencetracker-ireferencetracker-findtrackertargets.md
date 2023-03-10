---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTracker.FindTrackerTargets
title: IReferenceTracker::FindTrackerTargets (windows.ui.xaml.hosting.referencetracker.h)
description: Finds out what reference tracker targets are reachable from a reference tracker source; must be called by a garbage collector between calls to ReferenceTrackingStarted and FindTrackerTargetsCompleted.
helpviewer_keywords: ["FindTrackerTargets","FindTrackerTargets method [Windows Runtime]","FindTrackerTargets method [Windows Runtime]","IReferenceTracker interface","IReferenceTracker interface [Windows Runtime]","FindTrackerTargets method","IReferenceTracker.FindTrackerTargets","IReferenceTracker.xaml","IReferenceTracker::FindTrackerTargets","IReferenceTracker::xaml","windows/IReferenceTracker::FindTrackerTargets","winrt.ireferencetracker_findtrackertargets"]
old-location: winrt\ireferencetracker_findtrackertargets.htm
tech.root: WinRT
ms.assetid: ede8da3a-cef8-4741-950d-4303870ab10e
ms.date: 12/05/2018
ms.keywords: FindTrackerTargets, FindTrackerTargets method [Windows Runtime], FindTrackerTargets method [Windows Runtime],IReferenceTracker interface, IReferenceTracker interface [Windows Runtime],FindTrackerTargets method, IReferenceTracker.FindTrackerTargets, IReferenceTracker.xaml, IReferenceTracker::FindTrackerTargets, IReferenceTracker::xaml, windows/IReferenceTracker::FindTrackerTargets, winrt.ireferencetracker_findtrackertargets
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
 - IReferenceTracker::FindTrackerTargets
 - windows.ui.xaml.hosting.referencetracker/IReferenceTracker::FindTrackerTargets
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
 - IReferenceTracker.FindTrackerTargets
---

# IReferenceTracker::FindTrackerTargets (windows.ui.xaml.hosting.referencetracker.h)


## -description

Finds out what reference tracker targets are reachable from a reference tracker source; must be called by a garbage collector between calls to <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-referencetrackingstarted">ReferenceTrackingStarted</a> and <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-findtrackertargetscompleted">FindTrackerTargetsCompleted</a>.

## -parameters

### -param callback [in]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker">IReferenceTracker</a>
