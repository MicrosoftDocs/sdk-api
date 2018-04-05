---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerManager.FindTrackerTargetsCompleted
title: IReferenceTrackerManager::FindTrackerTargetsCompleted method
author: windows-driver-content
description: Indicates that a garbage collection system has finished making all the calls it needs to IReferenceTracker::FindTrackerTargets; by this time, XAML has pegged all reference tracker targets that it wants to protect.
old-location: winrt\ireferencetrackermanager_findtrackertargetscompleted.htm
old-project: WinRT
ms.assetid: 16e6f9ac-0466-4ada-ad72-278b3dba6a26
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: FindTrackerTargetsCompleted method [Windows Runtime], FindTrackerTargetsCompleted method [Windows Runtime], IReferenceTrackerManager interface, FindTrackerTargetsCompleted,IReferenceTrackerManager.FindTrackerTargetsCompleted, IReferenceTrackerManager, IReferenceTrackerManager interface [Windows Runtime], FindTrackerTargetsCompleted method, IReferenceTrackerManager::FindTrackerTargetsCompleted, windows/IReferenceTrackerManager::FindTrackerTargetsCompleted, winrt.ireferencetrackermanager_findtrackertargetscompleted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: windows.ui.xaml.hosting.referencetracker.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.ui.xaml.hosting.referencetracker.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TransportInformation
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windows.ui.xaml.hosting.referencetracker.h
api_name:
-	IReferenceTrackerManager.FindTrackerTargetsCompleted
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IReferenceTrackerManager::FindTrackerTargetsCompleted method


## -description


Indicates that a garbage collection system has finished making all the calls it needs to <a href="https://msdn.microsoft.com/ede8da3a-cef8-4741-950d-4303870ab10e">IReferenceTracker::FindTrackerTargets</a>;   by this time, XAML has pegged all reference tracker targets that it wants to protect.


## -parameters




### -param findFailed [in]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bdac39a0-a51a-49cc-b554-58450c722a46">IReferenceTrackerManager</a>
 

 

