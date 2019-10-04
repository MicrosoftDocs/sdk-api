---
UID: NN:directmanipulation.IDirectManipulationDeferContactService
title: IDirectManipulationDeferContactService (directmanipulation.h)
author: windows-sdk-content
description: Represents a service for managing associations between a contact and a viewport.
old-location: directmanipulation\idirectmanipulationdefercontactservice.htm
tech.root: directmanipulation
ms.assetid: 6063352F-39FF-4E8F-B836-3DA0A02BE523
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectManipulationDeferContactService, IDirectManipulationDeferContactService interface [Direct Manipulation], IDirectManipulationDeferContactService interface [Direct Manipulation],described, directmanipulation.idirectmanipulationdefercontactservice, directmanipulation/IDirectManipulationDeferContactService
ms.topic: interface
f1_keywords: 
 - "directmanipulation/IDirectManipulationDeferContactService"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationDeferContactService interface


## -description


Represents a service for managing associations between a contact and a viewport.


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> is called when a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/inputmsg/wm-pointerdown">WM_POINTERDOWN</a> message is received. Upon receiving a <b>WM_POINTERDOWN</b>, the application can use the coordinates of the input to hit-test and determine the viewports to which the contact is associated.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationDeferContactService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationDeferContactService</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-cancelcontact">CancelContact</a>
</td>
<td align="left" width="63%">
Cancel all scheduled calls to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> for this <i>pointerId</i>.   
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-canceldeferral">CancelDeferral</a>
</td>
<td align="left" width="63%">
Cancel the deferral set in <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact">DeferContact</a> and process the scheduled <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> call for this <i>pointerId</i>.   
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact">DeferContact</a>
</td>
<td align="left" width="63%">
Specifies the amount of time to defer the execution of a call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> for this <i>pointerId</i>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a>
 

 

