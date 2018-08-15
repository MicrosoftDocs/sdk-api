---
UID: NN:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost
title: IReferenceTrackerHost
author: windows-sdk-content
description: Defines an interface that provides the global services used by the garbage collection (GC) system used by the XAML framework.
old-location: winrt\ireferencetrackerhost.htm
old-project: WinRT
ms.assetid: b17fe8ae-be79-4281-a313-517505017401
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IReferenceTrackerHost, IReferenceTrackerHost interface [Windows Runtime], IReferenceTrackerHost interface [Windows Runtime],described, windows/IReferenceTrackerHost, winrt.ireferencetrackerhost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: windows.ui.xaml.hosting.referencetracker.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PDF_RENDER_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.ui.xaml.hosting.referencetracker.h
api_name:
 - IReferenceTrackerHost
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IReferenceTrackerHost interface


## -description


Defines an interface that provides the global services used by the garbage collection (GC) system used by the XAML framework.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceTrackerHost</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IReferenceTrackerHost</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReferenceTrackerHost</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e04381c-49b2-436b-9e92-ec13b88e42f1">AddMemoryPressure</a>
</td>
<td align="left" width="63%">
Informs the host of increased memory allocations since the last notification.
The CLR uses this to inform the algorithm that determines when to run a garbage collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c962299e-f813-45b8-a83b-1c1887e8c0f9">DisconnectUnusedReferenceSources</a>
</td>
<td align="left" width="63%">
Requests that the host perform a garbage collection and remove all unnecessary reference sources.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dabc7ce-a6aa-4acd-b331-3f74b0f2d179">GetTrackerTarget</a>
</td>
<td align="left" width="63%">
Requests the host to provide a reference tracker target that references a reference tracker source. This tracker target then controls the lifetime of the tracker source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14391c59-832c-441a-956a-090888d35c81">NotifyEndOfReferenceTrackingOnThread</a>
</td>
<td align="left" width="63%">
Notifies the host that reference tracking is no longer available on the calling thread; XAML calls this when the <b>FrameworkView</b> is uninitialized.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8b6f458-a9b9-41b7-a718-a193803842d8">ReleaseDisconnectedReferenceSources</a>
</td>
<td align="left" width="63%">
Requests that the host call <b>IUnknown::Release</b> on any reference tracker objects that have been disconnected by a reference source.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/686a8a17-d6a6-4062-9f14-add132685b66">RemoveMemoryPressure</a>
</td>
<td align="left" width="63%">
Informs the host of reduced memory allocations since the last notification.

</td>
</tr>
</table> 


## -remarks



An implementation of this interface must be registered with the XAML framework by passing it to the <a href="https://msdn.microsoft.com/02828d30-5023-4bd6-9c7a-8a3458462655">IReferenceTrackerManager::SetReferenceTrackerHost</a> method.



