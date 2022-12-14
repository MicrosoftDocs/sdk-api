---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerManager.ReferenceTrackingCompleted
title: IReferenceTrackerManager::ReferenceTrackingCompleted (windows.ui.xaml.hosting.referencetracker.h)
description: Indicates that a garbage collection system has finished with its collection process; at this point, XAML unblocks threads attempting to update tracked references.
helpviewer_keywords: ["IReferenceTrackerManager interface [Windows Runtime]","ReferenceTrackingCompleted method","IReferenceTrackerManager.ReferenceTrackingCompleted","IReferenceTrackerManager.xaml","IReferenceTrackerManager::ReferenceTrackingCompleted","IReferenceTrackerManager::xaml","ReferenceTrackingCompleted","ReferenceTrackingCompleted method [Windows Runtime]","ReferenceTrackingCompleted method [Windows Runtime]","IReferenceTrackerManager interface","windows/IReferenceTrackerManager::ReferenceTrackingCompleted","winrt.ireferencetrackermanager_referencetrackingcompleted"]
old-location: winrt\ireferencetrackermanager_referencetrackingcompleted.htm
tech.root: WinRT
ms.assetid: 17f3832f-c3cb-4797-8f48-c1cf0c9e408a
ms.date: 12/05/2018
ms.keywords: IReferenceTrackerManager interface [Windows Runtime],ReferenceTrackingCompleted method, IReferenceTrackerManager.ReferenceTrackingCompleted, IReferenceTrackerManager.xaml, IReferenceTrackerManager::ReferenceTrackingCompleted, IReferenceTrackerManager::xaml, ReferenceTrackingCompleted, ReferenceTrackingCompleted method [Windows Runtime], ReferenceTrackingCompleted method [Windows Runtime],IReferenceTrackerManager interface, windows/IReferenceTrackerManager::ReferenceTrackingCompleted, winrt.ireferencetrackermanager_referencetrackingcompleted
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
 - IReferenceTrackerManager::ReferenceTrackingCompleted
 - windows.ui.xaml.hosting.referencetracker/IReferenceTrackerManager::ReferenceTrackingCompleted
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
 - IReferenceTrackerManager.ReferenceTrackingCompleted
---

# IReferenceTrackerManager::ReferenceTrackingCompleted (windows.ui.xaml.hosting.referencetracker.h)


## -description

Indicates that a garbage collection system has finished with its collection process;  at this point, XAML unblocks threads attempting to update tracked references.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager">IReferenceTrackerManager</a>
