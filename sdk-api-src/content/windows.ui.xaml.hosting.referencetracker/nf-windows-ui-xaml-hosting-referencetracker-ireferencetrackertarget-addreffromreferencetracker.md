---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerTarget.AddRefFromReferenceTracker
title: IReferenceTrackerTarget::xaml (windows.ui.xaml.hosting.referencetracker.h)
author: windows-sdk-content
description: Indicates that the reference tracker is returning the target XAML object(s) from previous calls to FindTrackerTargets. Note that the reference is held by the reference tracker object in lieu of IUnknown::AddRef.
old-location: winrt\ireferencetrackertarget_addreffromreferencetracker.htm
tech.root: WinRT
ms.assetid: 91c02fd8-a210-4e6a-ab60-43ea7c1312be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddRefFromReferenceTracker, AddRefFromReferenceTracker method [Windows Runtime], AddRefFromReferenceTracker method [Windows Runtime],IReferenceTrackerTarget interface, IReferenceTrackerTarget interface [Windows Runtime],AddRefFromReferenceTracker method, IReferenceTrackerTarget.AddRefFromReferenceTracker, IReferenceTrackerTarget.xaml, IReferenceTrackerTarget::AddRefFromReferenceTracker, IReferenceTrackerTarget::xaml, windows/IReferenceTrackerTarget::AddRefFromReferenceTracker, winrt.ireferencetrackertarget_addreffromreferencetracker
ms.topic: method
f1_keywords: 
 - "windows.ui.xaml.hosting.referencetracker/IReferenceTrackerTarget.AddRefFromReferenceTracker"
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
 - IReferenceTrackerTarget.AddRefFromReferenceTracker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IReferenceTrackerTarget::xaml


## -description


Indicates that the reference tracker is returning the target XAML object(s) from previous calls to  <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets">FindTrackerTargets</a>.  Note that the reference is held by the reference tracker object in lieu of <b>IUnknown::AddRef</b>.


## -parameters






## -remarks



  When the XAML framework keeps this reference in lieu of a COM reference, it indicates that the framework must call your implementation of <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget-peg">Peg</a> to ensure that the target does not get collected.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget">IReferenceTrackerTarget</a>
 

 

