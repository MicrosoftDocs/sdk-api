---
UID: NN:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost
title: IReferenceTrackerHost (windows.ui.xaml.hosting.referencetracker.h)
description: Defines an interface that provides the global services used by the garbage collection (GC) system used by the XAML framework.
helpviewer_keywords: ["IReferenceTrackerHost","IReferenceTrackerHost interface [Windows Runtime]","IReferenceTrackerHost interface [Windows Runtime]","described","windows/IReferenceTrackerHost","winrt.ireferencetrackerhost"]
old-location: winrt\ireferencetrackerhost.htm
tech.root: WinRT
ms.assetid: b17fe8ae-be79-4281-a313-517505017401
ms.date: 12/05/2018
ms.keywords: IReferenceTrackerHost, IReferenceTrackerHost interface [Windows Runtime], IReferenceTrackerHost interface [Windows Runtime],described, windows/IReferenceTrackerHost, winrt.ireferencetrackerhost
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
 - IReferenceTrackerHost
 - windows.ui.xaml.hosting.referencetracker/IReferenceTrackerHost
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
 - IReferenceTrackerHost
---

# IReferenceTrackerHost interface


## -description

Defines an interface that provides the global services used by the garbage collection (GC) system used by the XAML framework.

## -inheritance

The <b>IReferenceTrackerHost</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReferenceTrackerHost</b> also has these types of members:

## -remarks

An implementation of this interface must be registered with the XAML framework by passing it to the <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager-setreferencetrackerhost">IReferenceTrackerManager::SetReferenceTrackerHost</a> method.
