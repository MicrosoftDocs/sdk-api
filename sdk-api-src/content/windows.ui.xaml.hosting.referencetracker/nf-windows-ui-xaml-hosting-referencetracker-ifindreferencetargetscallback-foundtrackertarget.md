---
UID: NF:windows.ui.xaml.hosting.referencetracker.IFindReferenceTargetsCallback.FoundTrackerTarget
title: IFindReferenceTargetsCallback::xaml (windows.ui.xaml.hosting.referencetracker.h)
description: Called whenever a XAML object reference tracker target is found.
helpviewer_keywords: ["FoundTrackerTarget","FoundTrackerTarget method [Windows Runtime]","FoundTrackerTarget method [Windows Runtime]","IFindReferenceTargetsCallback interface","IFindReferenceTargetsCallback interface [Windows Runtime]","FoundTrackerTarget method","IFindReferenceTargetsCallback.FoundTrackerTarget","IFindReferenceTargetsCallback.xaml","IFindReferenceTargetsCallback::FoundTrackerTarget","IFindReferenceTargetsCallback::xaml","windows/IFindReferenceTargetsCallback::FoundTrackerTarget","winrt.ifindreferencetargetscallback_foundtrackertarget"]
old-location: winrt\ifindreferencetargetscallback_foundtrackertarget.htm
tech.root: WinRT
ms.assetid: f8959af6-a857-4bca-a469-d68f70e2fadf
ms.date: 12/05/2018
ms.keywords: FoundTrackerTarget, FoundTrackerTarget method [Windows Runtime], FoundTrackerTarget method [Windows Runtime],IFindReferenceTargetsCallback interface, IFindReferenceTargetsCallback interface [Windows Runtime],FoundTrackerTarget method, IFindReferenceTargetsCallback.FoundTrackerTarget, IFindReferenceTargetsCallback.xaml, IFindReferenceTargetsCallback::FoundTrackerTarget, IFindReferenceTargetsCallback::xaml, windows/IFindReferenceTargetsCallback::FoundTrackerTarget, winrt.ifindreferencetargetscallback_foundtrackertarget
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
 - IFindReferenceTargetsCallback::FoundTrackerTarget
 - windows.ui.xaml.hosting.referencetracker/IFindReferenceTargetsCallback::FoundTrackerTarget
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
 - IFindReferenceTargetsCallback.FoundTrackerTarget
---

# IFindReferenceTargetsCallback::xaml


## -description

Called whenever a XAML object reference tracker target is found.

## -parameters

### -param target [in]

A XAML object reference tracker target instance found by the XAML object reference tracker manager.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ifindreferencetargetscallback">IFindReferenceTargetsCallback</a>