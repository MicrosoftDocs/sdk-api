---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTracker.FindTrackerTargets
title: IReferenceTracker::xaml
author: windows-sdk-content
description: Finds out what reference tracker targets are reachable from a reference tracker source; must be called by a garbage collector between calls to ReferenceTrackingStarted and FindTrackerTargetsCompleted.
old-location: winrt\ireferencetracker_findtrackertargets.htm
old-project: WinRT
ms.assetid: ede8da3a-cef8-4741-950d-4303870ab10e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FindTrackerTargets, FindTrackerTargets method [Windows Runtime], FindTrackerTargets method [Windows Runtime],IReferenceTracker interface, IReferenceTracker interface [Windows Runtime],FindTrackerTargets method, IReferenceTracker.FindTrackerTargets, IReferenceTracker.xaml, IReferenceTracker::FindTrackerTargets, IReferenceTracker::xaml, windows/IReferenceTracker::FindTrackerTargets, winrt.ireferencetracker_findtrackertargets
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: PDF_RENDER_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.ui.xaml.hosting.referencetracker.h
api_name:
 - IReferenceTracker.FindTrackerTargets
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IReferenceTracker::xaml


## -description


Finds out what reference tracker targets are reachable from a reference tracker source; must be called by a garbage collector between calls to <a href="https://msdn.microsoft.com/8d911bbb-aa5e-4906-86d6-caf6f3f84f6f">ReferenceTrackingStarted</a> and <a href="https://msdn.microsoft.com/16e6f9ac-0466-4ada-ad72-278b3dba6a26">FindTrackerTargetsCompleted</a>.  


## -parameters




### -param callback [in]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2267d29f-c3b2-4bc8-b4cb-6272a7ebae1a">IReferenceTracker</a>
 

 

