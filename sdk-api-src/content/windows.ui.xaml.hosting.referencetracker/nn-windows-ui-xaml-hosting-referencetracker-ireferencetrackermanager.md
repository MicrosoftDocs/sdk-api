---
UID: NN:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerManager
title: IReferenceTrackerManager
author: windows-sdk-content
description: Defines the interface for a XAML object reference manager. Implement this interface to manage instances of IReferenceTracker on XAML objects.
old-location: winrt\ireferencetrackermanager.htm
tech.root: WinRT
ms.assetid: bdac39a0-a51a-49cc-b554-58450c722a46
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IReferenceTrackerManager, IReferenceTrackerManager interface [Windows Runtime], IReferenceTrackerManager interface [Windows Runtime],described, windows/IReferenceTrackerManager, winrt.ireferencetrackermanager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IReferenceTrackerManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IReferenceTrackerManager interface


## -description


Defines the interface for  a XAML object reference manager. Implement this interface to manage instances of <a href="https://msdn.microsoft.com/2267d29f-c3b2-4bc8-b4cb-6272a7ebae1a">IReferenceTracker</a> on XAML objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceTrackerManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IReferenceTrackerManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReferenceTrackerManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16e6f9ac-0466-4ada-ad72-278b3dba6a26">FindTrackerTargetsCompleted</a>
</td>
<td align="left" width="63%">
Indicates that a garbage collection system has finished making all the calls it needs to <a href="https://msdn.microsoft.com/ede8da3a-cef8-4741-950d-4303870ab10e">IReferenceTracker::FindTrackerTargets</a>;   by this time, XAML has pegged all reference tracker targets that it wants to protect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17f3832f-c3cb-4797-8f48-c1cf0c9e408a">ReferenceTrackingCompleted</a>
</td>
<td align="left" width="63%">
Indicates that a garbage collection system has finished with its collection process;  at this point, XAML unblocks threads attempting to update tracked references.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d911bbb-aa5e-4906-86d6-caf6f3f84f6f">ReferenceTrackingStarted</a>
</td>
<td align="left" width="63%">
Indicates that a garbage collector is performing a collection; when the collection is finished, the garbage collector calls <a href="https://msdn.microsoft.com/16e6f9ac-0466-4ada-ad72-278b3dba6a26">FindTrackerTargetsCompleted</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02828d30-5023-4bd6-9c7a-8a3458462655">SetReferenceTrackerHost</a>
</td>
<td align="left" width="63%">
Registers an <a href="https://msdn.microsoft.com/b17fe8ae-be79-4281-a313-517505017401">IReferenceTrackerHost</a> interface with XAML.

</td>
</tr>
</table> 


## -remarks



Obtain a reference to an implementation of this interface by calling <a href="https://msdn.microsoft.com/c65f1220-24e6-4f63-9318-5b9e57d96e1b">IReferenceTracker::GetReferenceTrackerManager</a> on a XAML object that implements <a href="https://msdn.microsoft.com/2267d29f-c3b2-4bc8-b4cb-6272a7ebae1a">IReferenceTracker</a>.

There is only one instance of <b>IReferenceTrackerManager</b> for a process, and it may be called from any thread.



