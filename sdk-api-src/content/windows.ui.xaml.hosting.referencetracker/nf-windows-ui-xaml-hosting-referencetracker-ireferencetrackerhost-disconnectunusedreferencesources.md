---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost.DisconnectUnusedReferenceSources
title: IReferenceTrackerHost::DisconnectUnusedReferenceSources method
author: windows-driver-content
description: Requests that the host perform a garbage collection and remove all unnecessary reference sources.
old-location: winrt\ireferencetrackerhost_disconnectunusedreferencesources.htm
old-project: WinRT
ms.assetid: c962299e-f813-45b8-a83b-1c1887e8c0f9
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: DisconnectUnusedReferenceSources method [Windows Runtime], DisconnectUnusedReferenceSources method [Windows Runtime], IReferenceTrackerHost interface, DisconnectUnusedReferenceSources,IReferenceTrackerHost.DisconnectUnusedReferenceSources, IReferenceTrackerHost, IReferenceTrackerHost interface [Windows Runtime], DisconnectUnusedReferenceSources method, IReferenceTrackerHost::DisconnectUnusedReferenceSources, windows/IReferenceTrackerHost::DisconnectUnusedReferenceSources, winrt.ireferencetrackerhost_disconnectunusedreferencesources
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
-	IReferenceTrackerHost.DisconnectUnusedReferenceSources
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IReferenceTrackerHost::DisconnectUnusedReferenceSources method


## -description


Requests that the host perform a garbage collection and remove all unnecessary reference sources.  


## -parameters




### -param options [in]

May be 0 or 1; 1 indicates that an application suspend is in progress.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is expected to potentially cause the reference source to call <a href="https://msdn.microsoft.com/b4be9e74-6469-4f82-9748-036f08cec97f">IReferenceTracker::DisconnectFromTrackerSource</a>, but it is not necessary to call <b>IUnknown::Release</b> immediately on the tracker source.  In the CLR, this call triggers a garbage collection, but not a <b>WaitForPendingFinalizers</b>.  When flags is one, the garbage collection is executed in the <b>GCCollectionMode.Optimized</b> state.




## -see-also




<a href="https://msdn.microsoft.com/b17fe8ae-be79-4281-a313-517505017401">IReferenceTrackerHost</a>
 

 

