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

The <b>IReferenceTrackerManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReferenceTrackerManager</b> also has these types of members:

## -remarks

Obtain a reference to an implementation of this interface by calling <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-getreferencetrackermanager">IReferenceTracker::GetReferenceTrackerManager</a> on a XAML object that implements <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker">IReferenceTracker</a>.

There is only one instance of <b>IReferenceTrackerManager</b> for a process, and it may be called from any thread.
