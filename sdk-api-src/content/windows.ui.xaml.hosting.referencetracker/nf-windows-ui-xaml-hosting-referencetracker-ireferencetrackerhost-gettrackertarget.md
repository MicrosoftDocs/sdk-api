---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost.GetTrackerTarget
title: IReferenceTrackerHost::GetTrackerTarget (windows.ui.xaml.hosting.referencetracker.h)
description: Requests the host to provide a reference tracker target that references a reference tracker source. This tracker target then controls the lifetime of the tracker source.
helpviewer_keywords: ["GetTrackerTarget","GetTrackerTarget method [Windows Runtime]","GetTrackerTarget method [Windows Runtime]","IReferenceTrackerHost interface","IReferenceTrackerHost interface [Windows Runtime]","GetTrackerTarget method","IReferenceTrackerHost.GetTrackerTarget","IReferenceTrackerHost.xaml","IReferenceTrackerHost::GetTrackerTarget","IReferenceTrackerHost::xaml","windows/IReferenceTrackerHost::GetTrackerTarget","winrt.ireferencetrackerhost_gettrackertarget"]
old-location: winrt\ireferencetrackerhost_gettrackertarget.htm
tech.root: WinRT
ms.assetid: 5dabc7ce-a6aa-4acd-b331-3f74b0f2d179
ms.date: 12/05/2018
ms.keywords: GetTrackerTarget, GetTrackerTarget method [Windows Runtime], GetTrackerTarget method [Windows Runtime],IReferenceTrackerHost interface, IReferenceTrackerHost interface [Windows Runtime],GetTrackerTarget method, IReferenceTrackerHost.GetTrackerTarget, IReferenceTrackerHost.xaml, IReferenceTrackerHost::GetTrackerTarget, IReferenceTrackerHost::xaml, windows/IReferenceTrackerHost::GetTrackerTarget, winrt.ireferencetrackerhost_gettrackertarget
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
 - IReferenceTrackerHost::GetTrackerTarget
 - windows.ui.xaml.hosting.referencetracker/IReferenceTrackerHost::GetTrackerTarget
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
 - IReferenceTrackerHost.GetTrackerTarget
---

# IReferenceTrackerHost::GetTrackerTarget (windows.ui.xaml.hosting.referencetracker.h)


## -description

Requests the host to provide a reference tracker target that references a reference tracker source. This tracker target then controls the lifetime of the tracker source.

## -parameters

### -param unknown

The reference tracker source.

### -param newReference

The reference tracker target.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

  For example, after calling this method, calling <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget-peg">Peg</a> on the tracker target will prevent the tracker source from being collected.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost">IReferenceTrackerHost</a>
