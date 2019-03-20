---
UID: NN:directmanipulation.IDirectManipulationManager2
title: IDirectManipulationManager2 (directmanipulation.h)
author: windows-sdk-content
description: Extends the IDirectManipulationManager interface that provides access to all the Direct Manipulation features and APIs available to the client application.
old-location: directmanipulation\idirectmanipulationmanager2.htm
tech.root: directmanipulation
ms.assetid: 094C6C7D-F973-45AC-9B83-43DB9D46AF23
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectManipulationManager2, IDirectManipulationManager2 interface [Direct Manipulation], IDirectManipulationManager2 interface [Direct Manipulation],described, directmanipulation.idirectmanipulationmanager2, directmanipulation/IDirectManipulationManager2
ms.topic: interface
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - DirectManipulation.h
api_name:
 - IDirectManipulationManager2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationManager2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/d730a446-984e-4be0-aa7f-6d3dc93b2e34">IDirectManipulationManager</a> interface that provides access to all the <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> features and APIs available to the client application. 

The <b>IDirectManipulationManager2</b> interface adds support for configuration behaviors that can be attached to a viewport.
<div class="alert"><b>Note</b>  To obtain an <b>IDirectManipulationManager2</b> interface pointer, <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on an existing <a href="https://msdn.microsoft.com/d730a446-984e-4be0-aa7f-6d3dc93b2e34">IDirectManipulationManager</a> interface pointer.  </div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationManager2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8890E44F-595A-4116-B4A4-F10FAEE598B7">CreateBehavior</a>
</td>
<td align="left" width="63%">
Factory method to create a behavior.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

