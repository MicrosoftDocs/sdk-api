---
UID: NN:rdpencomapi.IRDPSRAPIInvitationManager
title: IRDPSRAPIInvitationManager (rdpencomapi.h)
description: Manages invitation objects.
helpviewer_keywords: ["IRDPSRAPIInvitationManager","IRDPSRAPIInvitationManager interface [RDP]","IRDPSRAPIInvitationManager interface [RDP]","described","rdp.irdpsrapiinvitationmanager","rdpencomapi/IRDPSRAPIInvitationManager"]
old-location: rdp\irdpsrapiinvitationmanager.htm
tech.root: rdp
ms.assetid: 300940ef-e8a6-4dd9-a078-d4325e20ae91
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIInvitationManager, IRDPSRAPIInvitationManager interface [RDP], IRDPSRAPIInvitationManager interface [RDP],described, rdp.irdpsrapiinvitationmanager, rdpencomapi/IRDPSRAPIInvitationManager
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPIInvitationManager
 - rdpencomapi/IRDPSRAPIInvitationManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIInvitationManager
---

# IRDPSRAPIInvitationManager interface


## -description

Manages invitation objects.

Applications obtain access to this object using <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-get_invitations">IRDPSRAPISharingSession::get_Invitations</a>


This interface provides access to the <b>RDPSRAPIInvitationManager</b> object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIInvitationManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRDPSRAPIInvitationManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRDPSRAPIInvitationManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiinvitationmanager-createinvitation">CreateInvitation</a>
</td>
<td align="left" width="63%">
Creates an invitation.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIInvitationManager</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiinvitationmanager-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An enumerator interface for the invitation collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiinvitationmanager-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The number of invitations in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiinvitationmanager-get_item">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An item in the invitation collection.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiinvitation">IRDPSRAPIInvitation</a>