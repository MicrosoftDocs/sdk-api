---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerManager.ReferenceTrackingStarted
title: IReferenceTrackerManager::ReferenceTrackingStarted (windows.ui.xaml.hosting.referencetracker.h)
description: Indicates that a garbage collector is performing a collection; when the collection is finished, the garbage collector calls FindTrackerTargetsCompleted.
helpviewer_keywords: ["IReferenceTrackerManager interface [Windows Runtime]","ReferenceTrackingStarted method","IReferenceTrackerManager.ReferenceTrackingStarted","IReferenceTrackerManager.xaml","IReferenceTrackerManager::ReferenceTrackingStarted","IReferenceTrackerManager::xaml","ReferenceTrackingStarted","ReferenceTrackingStarted method [Windows Runtime]","ReferenceTrackingStarted method [Windows Runtime]","IReferenceTrackerManager interface","windows/IReferenceTrackerManager::ReferenceTrackingStarted","winrt.ireferencetrackermanager_referencetrackingstarted"]
old-location: winrt\ireferencetrackermanager_referencetrackingstarted.htm
tech.root: WinRT
ms.assetid: 8d911bbb-aa5e-4906-86d6-caf6f3f84f6f
ms.date: 12/05/2018
ms.keywords: IReferenceTrackerManager interface [Windows Runtime],ReferenceTrackingStarted method, IReferenceTrackerManager.ReferenceTrackingStarted, IReferenceTrackerManager.xaml, IReferenceTrackerManager::ReferenceTrackingStarted, IReferenceTrackerManager::xaml, ReferenceTrackingStarted, ReferenceTrackingStarted method [Windows Runtime], ReferenceTrackingStarted method [Windows Runtime],IReferenceTrackerManager interface, windows/IReferenceTrackerManager::ReferenceTrackingStarted, winrt.ireferencetrackermanager_referencetrackingstarted
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
 - IReferenceTrackerManager::ReferenceTrackingStarted
 - windows.ui.xaml.hosting.referencetracker/IReferenceTrackerManager::ReferenceTrackingStarted
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
 - IReferenceTrackerManager.ReferenceTrackingStarted
---

# IReferenceTrackerManager::ReferenceTrackingStarted (windows.ui.xaml.hosting.referencetracker.h)


## -description

Indicates that a garbage collector is performing a collection; when the collection is finished, the garbage collector calls <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-findtrackertargetscompleted">FindTrackerTargetsCompleted</a>.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

  When this method is called, XAML blocks all threads where it is attempting to update tracked references.  Between calls to <b>ReferenceTrackingStarted</b> and <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-referencetrackingcompleted">ReferenceTrackingCompleted</a>, XAML does not make any calls to reference tracker target objects other than <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget-peg">Peg</a> and <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget-unpeg">Unpeg</a>.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager">IReferenceTrackerManager</a>
