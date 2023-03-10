---
UID: NN:windows.ui.xaml.hosting.referencetracker.IFindReferenceTargetsCallback
title: IFindReferenceTargetsCallback (windows.ui.xaml.hosting.referencetracker.h)
description: Defines the interface for callbacks from IReferenceTracker::FindTrackerTargets. The implementation of this interface must pass any IReferenceTrackerTarget instances it finds to the FoundTrackerTarget method.
helpviewer_keywords: ["IFindReferenceTargetsCallback","IFindReferenceTargetsCallback interface [Windows Runtime]","IFindReferenceTargetsCallback interface [Windows Runtime]","described","windows/IFindReferenceTargetsCallback","winrt.ifindreferencetargetscallback"]
old-location: winrt\ifindreferencetargetscallback.htm
tech.root: WinRT
ms.assetid: 1733680a-6b14-4541-b30d-407f5185ac14
ms.date: 12/05/2018
ms.keywords: IFindReferenceTargetsCallback, IFindReferenceTargetsCallback interface [Windows Runtime], IFindReferenceTargetsCallback interface [Windows Runtime],described, windows/IFindReferenceTargetsCallback, winrt.ifindreferencetargetscallback
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
 - IFindReferenceTargetsCallback
 - windows.ui.xaml.hosting.referencetracker/IFindReferenceTargetsCallback
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
 - IFindReferenceTargetsCallback
---

# IFindReferenceTargetsCallback interface


## -description

Defines the interface for callbacks from <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets">IReferenceTracker::FindTrackerTargets</a>. The implementation of this interface must pass any <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget">IReferenceTrackerTarget</a> instances it finds to the <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ifindreferencetargetscallback-foundtrackertarget">FoundTrackerTarget</a> method.

## -inheritance

The <b>IFindReferenceTargetsCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFindReferenceTargetsCallback</b> also has these types of members:

