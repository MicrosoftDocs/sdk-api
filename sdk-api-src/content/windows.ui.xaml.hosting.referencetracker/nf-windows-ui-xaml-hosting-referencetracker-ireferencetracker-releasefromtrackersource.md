---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTracker.ReleaseFromTrackerSource
title: IReferenceTracker::ReleaseFromTrackerSource (windows.ui.xaml.hosting.referencetracker.h)
description: Indicates each time that a tracker source calls IUnknown::Release on the reference tracker; must be called before the Release call.
helpviewer_keywords: ["IReferenceTracker interface [Windows Runtime]","ReleaseFromTrackerSource method","IReferenceTracker.ReleaseFromTrackerSource","IReferenceTracker.xaml","IReferenceTracker::ReleaseFromTrackerSource","IReferenceTracker::xaml","ReleaseFromTrackerSource","ReleaseFromTrackerSource method [Windows Runtime]","ReleaseFromTrackerSource method [Windows Runtime]","IReferenceTracker interface","windows/IReferenceTracker::ReleaseFromTrackerSource","winrt.ireferencetracker_releasefromtrackersource"]
old-location: winrt\ireferencetracker_releasefromtrackersource.htm
tech.root: WinRT
ms.assetid: 70ecc98e-30bd-48e6-966b-4b5955a58d8a
ms.date: 12/05/2018
ms.keywords: IReferenceTracker interface [Windows Runtime],ReleaseFromTrackerSource method, IReferenceTracker.ReleaseFromTrackerSource, IReferenceTracker.xaml, IReferenceTracker::ReleaseFromTrackerSource, IReferenceTracker::xaml, ReleaseFromTrackerSource, ReleaseFromTrackerSource method [Windows Runtime], ReleaseFromTrackerSource method [Windows Runtime],IReferenceTracker interface, windows/IReferenceTracker::ReleaseFromTrackerSource, winrt.ireferencetracker_releasefromtrackersource
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
 - IReferenceTracker::ReleaseFromTrackerSource
 - windows.ui.xaml.hosting.referencetracker/IReferenceTracker::ReleaseFromTrackerSource
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
 - IReferenceTracker.ReleaseFromTrackerSource
---

# IReferenceTracker::ReleaseFromTrackerSource (windows.ui.xaml.hosting.referencetracker.h)


## -description

Indicates each time that a tracker source calls <b>IUnknown::Release</b> on the reference tracker; must be called before the <b>Release</b> call.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker">IReferenceTracker</a>
