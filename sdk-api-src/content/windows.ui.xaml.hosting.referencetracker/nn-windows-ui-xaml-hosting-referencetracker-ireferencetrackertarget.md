---
UID: NN:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerTarget
title: IReferenceTrackerTarget
author: windows-sdk-content
description: Defines an interface implemented by a garbage collector object referenced from XAML.
old-location: winrt\ireferencetrackertarget.htm
tech.root: WinRT
ms.assetid: 204c647d-65c0-4b0e-b0fa-1abe9e8fdedd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IReferenceTrackerTarget, IReferenceTrackerTarget interface [Windows Runtime], IReferenceTrackerTarget interface [Windows Runtime],described, windows/IReferenceTrackerTarget, winrt.ireferencetrackertarget
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
 - IReferenceTrackerTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IReferenceTrackerTarget interface


## -description


Defines an interface implemented by a garbage collector object referenced from XAML.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReferenceTrackerTarget</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IReferenceTrackerTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReferenceTrackerTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91c02fd8-a210-4e6a-ab60-43ea7c1312be">AddRefFromReferenceTracker</a>
</td>
<td align="left" width="63%">
Indicates that the reference tracker is returning the target XAML object(s) from previous calls to  <a href="https://msdn.microsoft.com/ede8da3a-cef8-4741-950d-4303870ab10e">FindTrackerTargets</a>.  Note that the reference is held by the reference tracker object in lieu of <b>IUnknown::AddRef</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2750e8b1-eeeb-411a-89a8-b63b26f731ac">Peg</a>
</td>
<td align="left" width="63%">
Marks that the reference tracker target is in use by the XAML framework, and should not be collected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/646e6a3d-e7ea-4deb-ae1f-546caaaf4ea4">ReleaseFromReferenceTracker</a>
</td>
<td align="left" width="63%">
Releases the XAML object reference marked in a previous call to <a href="https://msdn.microsoft.com/91c02fd8-a210-4e6a-ab60-43ea7c1312be">AddRefFromReferenceTracker</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c070957f-3bf8-4e72-ad56-e9cb023692c6">Unpeg</a>
</td>
<td align="left" width="63%">
Marks that the reference tracker target is no longer in use by the XAML framework, and can be collected.  

</td>
</tr>
</table> 

