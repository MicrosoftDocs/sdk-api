---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost.ReleaseDisconnectedReferenceSources
title: IReferenceTrackerHost::ReleaseDisconnectedReferenceSources method
author: windows-driver-content
description: Requests that the host call IUnknown::Release on any reference tracker objects that have been disconnected by a reference source.
old-location: winrt\ireferencetrackerhost_releasedisconnectedreferencesources.htm
old-project: WinRT
ms.assetid: c8b6f458-a9b9-41b7-a718-a193803842d8
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IReferenceTrackerHost, IReferenceTrackerHost interface [Windows Runtime], ReleaseDisconnectedReferenceSources method, IReferenceTrackerHost::ReleaseDisconnectedReferenceSources, ReleaseDisconnectedReferenceSources method [Windows Runtime], ReleaseDisconnectedReferenceSources method [Windows Runtime], IReferenceTrackerHost interface, ReleaseDisconnectedReferenceSources,IReferenceTrackerHost.ReleaseDisconnectedReferenceSources, windows/IReferenceTrackerHost::ReleaseDisconnectedReferenceSources, winrt.ireferencetrackerhost_releasedisconnectedreferencesources
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: windows.ui.xaml.hosting.referencetracker.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.ui.xaml.hosting.referencetracker.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TransportInformation
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windows.ui.xaml.hosting.referencetracker.h
api_name:
-	IReferenceTrackerHost.ReleaseDisconnectedReferenceSources
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IReferenceTrackerHost::ReleaseDisconnectedReferenceSources method


## -description


Requests that the host call <b>IUnknown::Release</b> on any reference tracker objects that have been disconnected by a reference source.  


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is not necessary for the <b>Release</b> calls to come in on the same thread.
In this call, the CLR calls <b>WaitForPendingFinalizers</b>.





## -see-also




<a href="https://msdn.microsoft.com/b17fe8ae-be79-4281-a313-517505017401">IReferenceTrackerHost</a>
 

 

