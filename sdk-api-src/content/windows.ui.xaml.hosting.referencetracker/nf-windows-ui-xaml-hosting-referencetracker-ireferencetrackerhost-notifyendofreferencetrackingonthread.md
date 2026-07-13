---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost.NotifyEndOfReferenceTrackingOnThread
title: IReferenceTrackerHost::NotifyEndOfReferenceTrackingOnThread (windows.ui.xaml.hosting.referencetracker.h)
description: Notifies the host that reference tracking is no longer available on the calling thread; XAML calls this when the FrameworkView is uninitialized.
helpviewer_keywords: ["IReferenceTrackerHost interface [Windows Runtime]","NotifyEndOfReferenceTrackingOnThread method","IReferenceTrackerHost.NotifyEndOfReferenceTrackingOnThread","IReferenceTrackerHost.xaml","IReferenceTrackerHost::NotifyEndOfReferenceTrackingOnThread","IReferenceTrackerHost::xaml","NotifyEndOfReferenceTrackingOnThread","NotifyEndOfReferenceTrackingOnThread method [Windows Runtime]","NotifyEndOfReferenceTrackingOnThread method [Windows Runtime]","IReferenceTrackerHost interface","windows/IReferenceTrackerHost::NotifyEndOfReferenceTrackingOnThread","winrt.ireferencetrackerhost_notifyendofreferencetrackingonthread"]
old-location: winrt\ireferencetrackerhost_notifyendofreferencetrackingonthread.htm
tech.root: WinRT
ms.assetid: 14391c59-832c-441a-956a-090888d35c81
ms.date: 12/05/2018
ms.keywords: IReferenceTrackerHost interface [Windows Runtime],NotifyEndOfReferenceTrackingOnThread method, IReferenceTrackerHost.NotifyEndOfReferenceTrackingOnThread, IReferenceTrackerHost.xaml, IReferenceTrackerHost::NotifyEndOfReferenceTrackingOnThread, IReferenceTrackerHost::xaml, NotifyEndOfReferenceTrackingOnThread, NotifyEndOfReferenceTrackingOnThread method [Windows Runtime], NotifyEndOfReferenceTrackingOnThread method [Windows Runtime],IReferenceTrackerHost interface, windows/IReferenceTrackerHost::NotifyEndOfReferenceTrackingOnThread, winrt.ireferencetrackerhost_notifyendofreferencetrackingonthread
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
 - IReferenceTrackerHost::NotifyEndOfReferenceTrackingOnThread
 - windows.ui.xaml.hosting.referencetracker/IReferenceTrackerHost::NotifyEndOfReferenceTrackingOnThread
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
 - IReferenceTrackerHost.NotifyEndOfReferenceTrackingOnThread
---

# IReferenceTrackerHost::NotifyEndOfReferenceTrackingOnThread (windows.ui.xaml.hosting.referencetracker.h)


## -description

Notifies the host that reference tracking is no longer available on the calling thread; XAML calls this when the <b>FrameworkView</b> is uninitialized.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost">IReferenceTrackerHost</a>
