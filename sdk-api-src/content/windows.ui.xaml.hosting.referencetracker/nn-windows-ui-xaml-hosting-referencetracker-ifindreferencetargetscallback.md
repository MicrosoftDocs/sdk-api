---
UID: NN:windows.ui.xaml.hosting.referencetracker.IFindReferenceTargetsCallback
title: IFindReferenceTargetsCallback
author: windows-sdk-content
description: Defines the interface for callbacks from IReferenceTracker::FindTrackerTargets. The implementation of this interface must pass any IReferenceTrackerTarget instances it finds to the FoundTrackerTarget method.
old-location: winrt\ifindreferencetargetscallback.htm
tech.root: WinRT
ms.assetid: 1733680a-6b14-4541-b30d-407f5185ac14
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IFindReferenceTargetsCallback, IFindReferenceTargetsCallback interface [Windows Runtime], IFindReferenceTargetsCallback interface [Windows Runtime],described, windows/IFindReferenceTargetsCallback, winrt.ifindreferencetargetscallback
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFindReferenceTargetsCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFindReferenceTargetsCallback interface


## -description


Defines the interface for callbacks from <a href="https://msdn.microsoft.com/ede8da3a-cef8-4741-950d-4303870ab10e">IReferenceTracker::FindTrackerTargets</a>. The implementation of this interface must pass any <a href="https://msdn.microsoft.com/204c647d-65c0-4b0e-b0fa-1abe9e8fdedd">IReferenceTrackerTarget</a> instances it finds to the <a href="https://msdn.microsoft.com/f8959af6-a857-4bca-a469-d68f70e2fadf">FoundTrackerTarget</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFindReferenceTargetsCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFindReferenceTargetsCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFindReferenceTargetsCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8959af6-a857-4bca-a469-d68f70e2fadf">FoundTrackerTarget</a>
</td>
<td align="left" width="63%">
Called whenever a XAML object reference tracker target is found.

</td>
</tr>
</table> 

