---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTracker.DisconnectFromTrackerSource
title: IReferenceTracker::xaml (windows.ui.xaml.hosting.referencetracker.h)
author: windows-sdk-content
description: Indicates that a reference tracker source has stopped tracking a reference tracker.
old-location: winrt\ireferencetracker_disconnectfromtrackersource.htm
tech.root: WinRT
ms.assetid: b4be9e74-6469-4f82-9748-036f08cec97f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DisconnectFromTrackerSource, DisconnectFromTrackerSource method [Windows Runtime], DisconnectFromTrackerSource method [Windows Runtime],IReferenceTracker interface, IReferenceTracker interface [Windows Runtime],DisconnectFromTrackerSource method, IReferenceTracker.DisconnectFromTrackerSource, IReferenceTracker.xaml, IReferenceTracker::DisconnectFromTrackerSource, IReferenceTracker::xaml, windows/IReferenceTracker::DisconnectFromTrackerSource, winrt.ireferencetracker_disconnectfromtrackersource
ms.topic: method
f1_keywords: 
 - "windows.ui.xaml.hosting.referencetracker/IReferenceTracker.DisconnectFromTrackerSource"
dev_langs:
 - c++
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
 - IReferenceTracker.DisconnectFromTrackerSource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IReferenceTracker::xaml


## -description


Indicates that a reference tracker source has stopped tracking a reference tracker.  


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling this method does not indicate that the tracker source has released all COM references on the reference tracker.  
This method is called by the CLR during garbage collection when a runtime-callable wrapper is collected, but the XAML object does not get released until it is processed by the finalizer thread.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker">IReferenceTracker</a>
 

 

