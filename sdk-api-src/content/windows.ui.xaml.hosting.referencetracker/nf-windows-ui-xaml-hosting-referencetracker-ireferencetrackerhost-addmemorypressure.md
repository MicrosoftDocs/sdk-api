---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost.AddMemoryPressure
title: IReferenceTrackerHost::xaml
author: windows-sdk-content
description: Informs the host of increased memory allocations since the last notification. The CLR uses this to inform the algorithm that determines when to run a garbage collection.
old-location: winrt\ireferencetrackerhost_addmemorypressure.htm
tech.root: WinRT
ms.assetid: 1e04381c-49b2-436b-9e92-ec13b88e42f1
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AddMemoryPressure, AddMemoryPressure method [Windows Runtime], AddMemoryPressure method [Windows Runtime],IReferenceTrackerHost interface, IReferenceTrackerHost interface [Windows Runtime],AddMemoryPressure method, IReferenceTrackerHost.AddMemoryPressure, IReferenceTrackerHost.xaml, IReferenceTrackerHost::AddMemoryPressure, IReferenceTrackerHost::xaml, windows/IReferenceTrackerHost::AddMemoryPressure, winrt.ireferencetrackerhost_addmemorypressure
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IReferenceTrackerHost.AddMemoryPressure
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IReferenceTrackerHost::xaml


## -description


Informs the host of increased memory allocations since the last notification.
The CLR uses this to inform the algorithm that determines when to run a garbage collection.



## -parameters




### -param bytesAllocated

TBD




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b17fe8ae-be79-4281-a313-517505017401">IReferenceTrackerHost</a>
 

 

