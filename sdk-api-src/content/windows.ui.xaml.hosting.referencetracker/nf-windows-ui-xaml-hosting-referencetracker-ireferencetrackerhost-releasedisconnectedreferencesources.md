---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost.ReleaseDisconnectedReferenceSources
title: IReferenceTrackerHost::xaml (windows.ui.xaml.hosting.referencetracker.h)
author: windows-sdk-content
description: Requests that the host call IUnknown::Release on any reference tracker objects that have been disconnected by a reference source.
old-location: winrt\ireferencetrackerhost_releasedisconnectedreferencesources.htm
tech.root: WinRT
ms.assetid: c8b6f458-a9b9-41b7-a718-a193803842d8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IReferenceTrackerHost interface [Windows Runtime],ReleaseDisconnectedReferenceSources method, IReferenceTrackerHost.ReleaseDisconnectedReferenceSources, IReferenceTrackerHost.xaml, IReferenceTrackerHost::ReleaseDisconnectedReferenceSources, IReferenceTrackerHost::xaml, ReleaseDisconnectedReferenceSources, ReleaseDisconnectedReferenceSources method [Windows Runtime], ReleaseDisconnectedReferenceSources method [Windows Runtime],IReferenceTrackerHost interface, windows/IReferenceTrackerHost::ReleaseDisconnectedReferenceSources, winrt.ireferencetrackerhost_releasedisconnectedreferencesources
ms.topic: method
f1_keywords: 
 - "windows.ui.xaml.hosting.referencetracker/IReferenceTrackerHost.ReleaseDisconnectedReferenceSources"
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
 - IReferenceTrackerHost.ReleaseDisconnectedReferenceSources
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IReferenceTrackerHost::xaml


## -description


Requests that the host call <b>IUnknown::Release</b> on any reference tracker objects that have been disconnected by a reference source.  


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is not necessary for the <b>Release</b> calls to come in on the same thread.
In this call, the CLR calls <b>WaitForPendingFinalizers</b>.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost">IReferenceTrackerHost</a>
 

 

