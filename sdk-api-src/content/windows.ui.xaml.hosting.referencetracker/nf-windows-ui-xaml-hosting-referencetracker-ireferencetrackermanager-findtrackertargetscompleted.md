---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerManager.FindTrackerTargetsCompleted
title: IReferenceTrackerManager::FindTrackerTargetsCompleted (windows.ui.xaml.hosting.referencetracker.h)
description: Indicates that a garbage collection system has finished making all the calls it needs to IReferenceTracker::FindTrackerTargets; by this time, XAML has pegged all reference tracker targets that it wants to protect.
helpviewer_keywords: ["FindTrackerTargetsCompleted","FindTrackerTargetsCompleted method [Windows Runtime]","FindTrackerTargetsCompleted method [Windows Runtime]","IReferenceTrackerManager interface","IReferenceTrackerManager interface [Windows Runtime]","FindTrackerTargetsCompleted method","IReferenceTrackerManager.FindTrackerTargetsCompleted","IReferenceTrackerManager.xaml","IReferenceTrackerManager::FindTrackerTargetsCompleted","IReferenceTrackerManager::xaml","windows/IReferenceTrackerManager::FindTrackerTargetsCompleted","winrt.ireferencetrackermanager_findtrackertargetscompleted"]
old-location: winrt\ireferencetrackermanager_findtrackertargetscompleted.htm
tech.root: WinRT
ms.assetid: 16e6f9ac-0466-4ada-ad72-278b3dba6a26
ms.date: 12/05/2018
ms.keywords: FindTrackerTargetsCompleted, FindTrackerTargetsCompleted method [Windows Runtime], FindTrackerTargetsCompleted method [Windows Runtime],IReferenceTrackerManager interface, IReferenceTrackerManager interface [Windows Runtime],FindTrackerTargetsCompleted method, IReferenceTrackerManager.FindTrackerTargetsCompleted, IReferenceTrackerManager.xaml, IReferenceTrackerManager::FindTrackerTargetsCompleted, IReferenceTrackerManager::xaml, windows/IReferenceTrackerManager::FindTrackerTargetsCompleted, winrt.ireferencetrackermanager_findtrackertargetscompleted
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
 - IReferenceTrackerManager::FindTrackerTargetsCompleted
 - windows.ui.xaml.hosting.referencetracker/IReferenceTrackerManager::FindTrackerTargetsCompleted
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
 - IReferenceTrackerManager.FindTrackerTargetsCompleted
---

# IReferenceTrackerManager::FindTrackerTargetsCompleted (windows.ui.xaml.hosting.referencetracker.h)


## -description

Indicates that a garbage collection system has finished making all the calls it needs to <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets">IReferenceTracker::FindTrackerTargets</a>;   by this time, XAML has pegged all reference tracker targets that it wants to protect.

## -parameters

### -param findFailed [in]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager">IReferenceTrackerManager</a>
