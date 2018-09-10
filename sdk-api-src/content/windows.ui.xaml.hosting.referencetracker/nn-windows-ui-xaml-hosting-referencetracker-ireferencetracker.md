---
UID: NN:windows.ui.xaml.hosting.referencetracker.IReferenceTracker
title: IReferenceTracker
author: windows-sdk-content
description: Defines the interface implemented by the XAML framework for managing XAML object references.
old-location: winrt\ireferencetracker.htm
tech.root: WinRT
ms.assetid: 2267d29f-c3b2-4bc8-b4cb-6272a7ebae1a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IReferenceTracker, IReferenceTracker interface [Windows Runtime], IReferenceTracker interface [Windows Runtime],described, windows/IReferenceTracker, winrt.ireferencetracker
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
 - IReferenceTracker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IReferenceTracker interface


## -description


Defines the interface implemented by the XAML framework for managing XAML object references.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceTracker</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IReferenceTracker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReferenceTracker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce2100df-c0d9-4225-9053-ecba08533a04">AddRefFromTrackerSource</a>
</td>
<td align="left" width="63%">
Indicates each time that a tracker source calls <b>IUnknown::AddRef</b> on the reference tracker; called after the <b>AddRef</b> call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c5a0eaf-01a9-476c-8c71-1c817aa41fae">ConnectFromTrackerSource</a>
</td>
<td align="left" width="63%">
Indicates that a reference tracker source has created its first COM reference on a reference tracker object.  


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4be9e74-6469-4f82-9748-036f08cec97f">DisconnectFromTrackerSource</a>
</td>
<td align="left" width="63%">
Indicates that a reference tracker source has stopped tracking a reference tracker.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ede8da3a-cef8-4741-950d-4303870ab10e">FindTrackerTargets</a>
</td>
<td align="left" width="63%">
Finds out what reference tracker targets are reachable from a reference tracker source; must be called by a garbage collector between calls to <a href="https://msdn.microsoft.com/8d911bbb-aa5e-4906-86d6-caf6f3f84f6f">ReferenceTrackingStarted</a> and <a href="https://msdn.microsoft.com/16e6f9ac-0466-4ada-ad72-278b3dba6a26">FindTrackerTargetsCompleted</a>.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c65f1220-24e6-4f63-9318-5b9e57d96e1b">GetReferenceTrackerManager</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/bdac39a0-a51a-49cc-b554-58450c722a46">IReferenceTrackerManager</a> interface from a XAML object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca35bcf5-add0-47a8-b989-f6d69674ca30">PegFromTrackerSource</a>
</td>
<td align="left" width="63%">
Indicates that a tracker source is unable to protected a reference tracker object.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70ecc98e-30bd-48e6-966b-4b5955a58d8a">ReleaseFromTrackerSource</a>
</td>
<td align="left" width="63%">
Indicates each time that a tracker source calls <b>IUnknown::Release</b> on the reference tracker; must be called before the <b>Release</b> call.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by most XAML framework objects. It is not defined as <b>agile</b>, nor does it marshal across apartments. Use it only from within the apartment of the XAML object that implements it.



