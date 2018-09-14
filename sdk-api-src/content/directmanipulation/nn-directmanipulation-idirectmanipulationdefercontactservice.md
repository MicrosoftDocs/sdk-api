---
UID: NN:directmanipulation.IDirectManipulationDeferContactService
title: IDirectManipulationDeferContactService
author: windows-sdk-content
description: Represents a service for managing associations between a contact and a viewport.
old-location: directmanipulation\idirectmanipulationdefercontactservice.htm
tech.root: directmanipulation
ms.assetid: 6063352F-39FF-4E8F-B836-3DA0A02BE523
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDirectManipulationDeferContactService, IDirectManipulationDeferContactService interface [Direct Manipulation], IDirectManipulationDeferContactService interface [Direct Manipulation],described, directmanipulation.idirectmanipulationdefercontactservice, directmanipulation/IDirectManipulationDeferContactService
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
 - IDirectManipulationDeferContactService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationDeferContactService interface


## -description


Represents a service for managing associations between a contact and a viewport.


<a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> is called when a <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> message is received. Upon receiving a <b>WM_POINTERDOWN</b>, the application can use the coordinates of the input to hit-test and determine the viewports to which the contact is associated.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationDeferContactService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationDeferContactService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationDeferContactService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5C5029E5-CA4B-4853-B9D3-B99E869A44C3">CancelContact</a>
</td>
<td align="left" width="63%">
Cancel all scheduled calls to <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> for this <i>pointerId</i>.   
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/946F8CF8-6A6D-4BC1-B9BA-91D5B4A8A178">CancelDeferral</a>
</td>
<td align="left" width="63%">
Cancel the deferral set in <a href="https://msdn.microsoft.com/DEC97DD5-E43F-4541-8A80-D20EC8026493">DeferContact</a> and process the scheduled <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> call for this <i>pointerId</i>.   
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DEC97DD5-E43F-4541-8A80-D20EC8026493">DeferContact</a>
</td>
<td align="left" width="63%">
Specifies the amount of time to defer the execution of a call to <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> for this <i>pointerId</i>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>



<a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a>
 

 

