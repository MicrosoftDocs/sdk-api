---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTracker.AddRefFromTrackerSource
title: IReferenceTracker::AddRefFromTrackerSource (windows.ui.xaml.hosting.referencetracker.h)
description: Indicates each time that a tracker source calls IUnknown::AddRef on the reference tracker; called after the AddRef call.
helpviewer_keywords: ["AddRefFromTrackerSource","AddRefFromTrackerSource method [Windows Runtime]","AddRefFromTrackerSource method [Windows Runtime]","IReferenceTracker interface","IReferenceTracker interface [Windows Runtime]","AddRefFromTrackerSource method","IReferenceTracker.AddRefFromTrackerSource","IReferenceTracker.xaml","IReferenceTracker::AddRefFromTrackerSource","IReferenceTracker::xaml","windows/IReferenceTracker::AddRefFromTrackerSource","winrt.ireferencetracker_addreffromtrackersource"]
old-location: winrt\ireferencetracker_addreffromtrackersource.htm
tech.root: WinRT
ms.assetid: ce2100df-c0d9-4225-9053-ecba08533a04
ms.date: 12/05/2018
ms.keywords: AddRefFromTrackerSource, AddRefFromTrackerSource method [Windows Runtime], AddRefFromTrackerSource method [Windows Runtime],IReferenceTracker interface, IReferenceTracker interface [Windows Runtime],AddRefFromTrackerSource method, IReferenceTracker.AddRefFromTrackerSource, IReferenceTracker.xaml, IReferenceTracker::AddRefFromTrackerSource, IReferenceTracker::xaml, windows/IReferenceTracker::AddRefFromTrackerSource, winrt.ireferencetracker_addreffromtrackersource
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
 - IReferenceTracker::AddRefFromTrackerSource
 - windows.ui.xaml.hosting.referencetracker/IReferenceTracker::AddRefFromTrackerSource
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
 - IReferenceTracker.AddRefFromTrackerSource
---

# IReferenceTracker::AddRefFromTrackerSource (windows.ui.xaml.hosting.referencetracker.h)


## -description

Indicates each time that a tracker source calls <b>IUnknown::AddRef</b> on the reference tracker; called after the <b>AddRef</b> call.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker">IReferenceTracker</a>
