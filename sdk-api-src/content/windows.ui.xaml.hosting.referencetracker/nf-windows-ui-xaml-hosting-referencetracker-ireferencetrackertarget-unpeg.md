---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerTarget.Unpeg
title: IReferenceTrackerTarget::Unpeg (windows.ui.xaml.hosting.referencetracker.h)
description: Marks that the reference tracker target is no longer in use by the XAML framework, and can be collected.
helpviewer_keywords: ["IReferenceTrackerTarget interface [Windows Runtime]","Unpeg method","IReferenceTrackerTarget.Unpeg","IReferenceTrackerTarget.xaml","IReferenceTrackerTarget::Unpeg","IReferenceTrackerTarget::xaml","Unpeg","Unpeg method [Windows Runtime]","Unpeg method [Windows Runtime]","IReferenceTrackerTarget interface","windows/IReferenceTrackerTarget::Unpeg","winrt.ireferencetrackertarget_unpeg"]
old-location: winrt\ireferencetrackertarget_unpeg.htm
tech.root: WinRT
ms.assetid: c070957f-3bf8-4e72-ad56-e9cb023692c6
ms.date: 12/05/2018
ms.keywords: IReferenceTrackerTarget interface [Windows Runtime],Unpeg method, IReferenceTrackerTarget.Unpeg, IReferenceTrackerTarget.xaml, IReferenceTrackerTarget::Unpeg, IReferenceTrackerTarget::xaml, Unpeg, Unpeg method [Windows Runtime], Unpeg method [Windows Runtime],IReferenceTrackerTarget interface, windows/IReferenceTrackerTarget::Unpeg, winrt.ireferencetrackertarget_unpeg
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
 - IReferenceTrackerTarget::Unpeg
 - windows.ui.xaml.hosting.referencetracker/IReferenceTrackerTarget::Unpeg
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
 - IReferenceTrackerTarget.Unpeg
---

# IReferenceTrackerTarget::Unpeg (windows.ui.xaml.hosting.referencetracker.h)


## -description

Marks that the reference tracker target is no longer in use by the XAML framework, and can be collected.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  You do not need to have parity between calls to <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget-peg">Peg</a> and <b>Unpeg</b>. A single call to <b>Unpeg</b> will remove the marker set in all previous calls to <b>Peg</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget">IReferenceTrackerTarget</a>
