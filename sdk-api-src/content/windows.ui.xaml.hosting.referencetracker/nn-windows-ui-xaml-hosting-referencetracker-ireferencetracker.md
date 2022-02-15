---
UID: NN:windows.ui.xaml.hosting.referencetracker.IReferenceTracker
title: IReferenceTracker (windows.ui.xaml.hosting.referencetracker.h)
description: Defines the interface implemented by the XAML framework for managing XAML object references.
helpviewer_keywords: ["IReferenceTracker","IReferenceTracker interface [Windows Runtime]","IReferenceTracker interface [Windows Runtime]","described","windows/IReferenceTracker","winrt.ireferencetracker"]
old-location: winrt\ireferencetracker.htm
tech.root: WinRT
ms.assetid: 2267d29f-c3b2-4bc8-b4cb-6272a7ebae1a
ms.date: 12/05/2018
ms.keywords: IReferenceTracker, IReferenceTracker interface [Windows Runtime], IReferenceTracker interface [Windows Runtime],described, windows/IReferenceTracker, winrt.ireferencetracker
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
 - IReferenceTracker
 - windows.ui.xaml.hosting.referencetracker/IReferenceTracker
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
 - IReferenceTracker
---

# IReferenceTracker interface


## -description

Defines the interface implemented by the XAML framework for managing XAML object references.

## -inheritance

The <b>IReferenceTracker</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReferenceTracker</b> also has these types of members:

## -remarks

This interface is implemented by most XAML framework objects. It is not defined as <b>agile</b>, nor does it marshal across apartments. Use it only from within the apartment of the XAML object that implements it.
