---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost.RemoveMemoryPressure
title: IReferenceTrackerHost::RemoveMemoryPressure (windows.ui.xaml.hosting.referencetracker.h)
description: Informs the host of reduced memory allocations since the last notification.
helpviewer_keywords: ["IReferenceTrackerHost interface [Windows Runtime]","RemoveMemoryPressure method","IReferenceTrackerHost.RemoveMemoryPressure","IReferenceTrackerHost.xaml","IReferenceTrackerHost::RemoveMemoryPressure","IReferenceTrackerHost::xaml","RemoveMemoryPressure","RemoveMemoryPressure method [Windows Runtime]","RemoveMemoryPressure method [Windows Runtime]","IReferenceTrackerHost interface","windows/IReferenceTrackerHost::RemoveMemoryPressure","winrt.ireferencetrackerhost_removememorypressure"]
old-location: winrt\ireferencetrackerhost_removememorypressure.htm
tech.root: WinRT
ms.assetid: 686a8a17-d6a6-4062-9f14-add132685b66
ms.date: 12/05/2018
ms.keywords: IReferenceTrackerHost interface [Windows Runtime],RemoveMemoryPressure method, IReferenceTrackerHost.RemoveMemoryPressure, IReferenceTrackerHost.xaml, IReferenceTrackerHost::RemoveMemoryPressure, IReferenceTrackerHost::xaml, RemoveMemoryPressure, RemoveMemoryPressure method [Windows Runtime], RemoveMemoryPressure method [Windows Runtime],IReferenceTrackerHost interface, windows/IReferenceTrackerHost::RemoveMemoryPressure, winrt.ireferencetrackerhost_removememorypressure
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
 - IReferenceTrackerHost::RemoveMemoryPressure
 - windows.ui.xaml.hosting.referencetracker/IReferenceTrackerHost::RemoveMemoryPressure
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
 - IReferenceTrackerHost.RemoveMemoryPressure
---

# IReferenceTrackerHost::RemoveMemoryPressure (windows.ui.xaml.hosting.referencetracker.h)


## -description

Informs the host of reduced memory allocations since the last notification.

## -parameters

### -param bytesAllocated

The number of bytes currently allocated.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost">IReferenceTrackerHost</a>
