---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost.DisconnectUnusedReferenceSources
title: IReferenceTrackerHost::DisconnectUnusedReferenceSources (windows.ui.xaml.hosting.referencetracker.h)
description: Requests that the host perform a garbage collection and remove all unnecessary reference sources.
helpviewer_keywords: ["DisconnectUnusedReferenceSources","DisconnectUnusedReferenceSources method [Windows Runtime]","DisconnectUnusedReferenceSources method [Windows Runtime]","IReferenceTrackerHost interface","IReferenceTrackerHost interface [Windows Runtime]","DisconnectUnusedReferenceSources method","IReferenceTrackerHost.DisconnectUnusedReferenceSources","IReferenceTrackerHost.xaml","IReferenceTrackerHost::DisconnectUnusedReferenceSources","IReferenceTrackerHost::xaml","windows/IReferenceTrackerHost::DisconnectUnusedReferenceSources","winrt.ireferencetrackerhost_disconnectunusedreferencesources"]
old-location: winrt\ireferencetrackerhost_disconnectunusedreferencesources.htm
tech.root: WinRT
ms.assetid: c962299e-f813-45b8-a83b-1c1887e8c0f9
ms.date: 12/05/2018
ms.keywords: DisconnectUnusedReferenceSources, DisconnectUnusedReferenceSources method [Windows Runtime], DisconnectUnusedReferenceSources method [Windows Runtime],IReferenceTrackerHost interface, IReferenceTrackerHost interface [Windows Runtime],DisconnectUnusedReferenceSources method, IReferenceTrackerHost.DisconnectUnusedReferenceSources, IReferenceTrackerHost.xaml, IReferenceTrackerHost::DisconnectUnusedReferenceSources, IReferenceTrackerHost::xaml, windows/IReferenceTrackerHost::DisconnectUnusedReferenceSources, winrt.ireferencetrackerhost_disconnectunusedreferencesources
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
 - IReferenceTrackerHost::DisconnectUnusedReferenceSources
 - windows.ui.xaml.hosting.referencetracker/IReferenceTrackerHost::DisconnectUnusedReferenceSources
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
 - IReferenceTrackerHost.DisconnectUnusedReferenceSources
---

# IReferenceTrackerHost::DisconnectUnusedReferenceSources (windows.ui.xaml.hosting.referencetracker.h)


## -description

Requests that the host perform a garbage collection and remove all unnecessary reference sources.

## -parameters

### -param options [in]

May be 0 or 1; 1 indicates that an application suspend is in progress.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is expected to potentially cause the reference source to call <a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-disconnectfromtrackersource">IReferenceTracker::DisconnectFromTrackerSource</a>, but it is not necessary to call <b>IUnknown::Release</b> immediately on the tracker source.  In the CLR, this call triggers a garbage collection, but not a <b>WaitForPendingFinalizers</b>.  When flags is one, the garbage collection is executed in the <b>GCCollectionMode.Optimized</b> state.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost">IReferenceTrackerHost</a>
