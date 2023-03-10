---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTracker.ConnectFromTrackerSource
title: IReferenceTracker::ConnectFromTrackerSource (windows.ui.xaml.hosting.referencetracker.h)
description: Indicates that a reference tracker source has created its first COM reference on a reference tracker object.
helpviewer_keywords: ["ConnectFromTrackerSource","ConnectFromTrackerSource method [Windows Runtime]","ConnectFromTrackerSource method [Windows Runtime]","IReferenceTracker interface","IReferenceTracker interface [Windows Runtime]","ConnectFromTrackerSource method","IReferenceTracker.ConnectFromTrackerSource","IReferenceTracker.xaml","IReferenceTracker::ConnectFromTrackerSource","IReferenceTracker::xaml","windows/IReferenceTracker::ConnectFromTrackerSource","winrt.ireferencetracker_connectfromtrackersource"]
old-location: winrt\ireferencetracker_connectfromtrackersource.htm
tech.root: WinRT
ms.assetid: 7c5a0eaf-01a9-476c-8c71-1c817aa41fae
ms.date: 12/05/2018
ms.keywords: ConnectFromTrackerSource, ConnectFromTrackerSource method [Windows Runtime], ConnectFromTrackerSource method [Windows Runtime],IReferenceTracker interface, IReferenceTracker interface [Windows Runtime],ConnectFromTrackerSource method, IReferenceTracker.ConnectFromTrackerSource, IReferenceTracker.xaml, IReferenceTracker::ConnectFromTrackerSource, IReferenceTracker::xaml, windows/IReferenceTracker::ConnectFromTrackerSource, winrt.ireferencetracker_connectfromtrackersource
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
 - IReferenceTracker::ConnectFromTrackerSource
 - windows.ui.xaml.hosting.referencetracker/IReferenceTracker::ConnectFromTrackerSource
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
 - IReferenceTracker.ConnectFromTrackerSource
---

# IReferenceTracker::ConnectFromTrackerSource (windows.ui.xaml.hosting.referencetracker.h)


## -description

Indicates that a reference tracker source has created its first COM reference on a reference tracker object.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called, for example, when a runtime-callable wrapper is created to a XAML object, such as when a XAML object is returned as an <b>out</b> parameter argument.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker">IReferenceTracker</a>
