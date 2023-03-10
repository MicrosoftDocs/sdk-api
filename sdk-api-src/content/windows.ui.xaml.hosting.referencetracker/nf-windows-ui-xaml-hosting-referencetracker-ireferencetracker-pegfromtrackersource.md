---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTracker.PegFromTrackerSource
title: IReferenceTracker::PegFromTrackerSource (windows.ui.xaml.hosting.referencetracker.h)
description: Indicates that a tracker source is unable to protected a reference tracker object.
helpviewer_keywords: ["IReferenceTracker interface [Windows Runtime]","PegFromTrackerSource method","IReferenceTracker.PegFromTrackerSource","IReferenceTracker.xaml","IReferenceTracker::PegFromTrackerSource","IReferenceTracker::xaml","PegFromTrackerSource","PegFromTrackerSource method [Windows Runtime]","PegFromTrackerSource method [Windows Runtime]","IReferenceTracker interface","windows/IReferenceTracker::PegFromTrackerSource","winrt.ireferencetracker_pegfromtrackersource"]
old-location: winrt\ireferencetracker_pegfromtrackersource.htm
tech.root: WinRT
ms.assetid: ca35bcf5-add0-47a8-b989-f6d69674ca30
ms.date: 12/05/2018
ms.keywords: IReferenceTracker interface [Windows Runtime],PegFromTrackerSource method, IReferenceTracker.PegFromTrackerSource, IReferenceTracker.xaml, IReferenceTracker::PegFromTrackerSource, IReferenceTracker::xaml, PegFromTrackerSource, PegFromTrackerSource method [Windows Runtime], PegFromTrackerSource method [Windows Runtime],IReferenceTracker interface, windows/IReferenceTracker::PegFromTrackerSource, winrt.ireferencetracker_pegfromtrackersource
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
 - IReferenceTracker::PegFromTrackerSource
 - windows.ui.xaml.hosting.referencetracker/IReferenceTracker::PegFromTrackerSource
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
 - IReferenceTracker.PegFromTrackerSource
---

# IReferenceTracker::PegFromTrackerSource (windows.ui.xaml.hosting.referencetracker.h)


## -description

Indicates that a tracker source is unable to protected a reference tracker object.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by the CLR when it is returning a XAML object as an <b>out</b> parameter argument.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker">IReferenceTracker</a>
