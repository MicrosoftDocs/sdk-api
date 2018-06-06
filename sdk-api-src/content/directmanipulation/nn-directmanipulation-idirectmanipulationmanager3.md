---
UID: NN:directmanipulation.IDirectManipulationManager3
title: IDirectManipulationManager3
author: windows-sdk-content
description: Extends the IDirectManipulationManager2 interface that provides access to all the Direct Manipulation features and APIs available to the client application.
old-location: directmanipulation\idirectmanipulationmanager3.htm
old-project: directmanipulation
ms.assetid: 566d4a36-5623-4896-b23b-3824551850b0
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDirectManipulationManager3, IDirectManipulationManager3 interface [Direct Manipulation], IDirectManipulationManager3 interface [Direct Manipulation],described, directmanipulation.idirectmanipulationmanager3, directmanipulation/IDirectManipulationManager3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationManager3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationManager3 interface


## -description


Extends the <a href="https://msdn.microsoft.com/094C6C7D-F973-45AC-9B83-43DB9D46AF23">IDirectManipulationManager2</a> interface that provides access to all the <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> features and APIs available to the client application. 

The <b>IDirectManipulationManager3</b> interface adds support for retrieving an <a href="https://msdn.microsoft.com/6063352F-39FF-4E8F-B836-3DA0A02BE523">IDirectManipulationDeferContactService</a> object.
<div class="alert"><b>Note</b>  To obtain an <b>IDirectManipulationManager3</b> interface pointer, <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on an existing <a href="https://msdn.microsoft.com/d730a446-984e-4be0-aa7f-6d3dc93b2e34">IDirectManipulationManager</a> interface pointer.  </div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationManager3</b> interface inherits from <b>IDirectManipulationManager2</b>. <b>IDirectManipulationManager3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationManager3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36f46402-ed71-41d8-8df5-02ef59819bb3">GetService</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/6063352F-39FF-4E8F-B836-3DA0A02BE523">IDirectManipulationDeferContactService</a> object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

