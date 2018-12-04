---
UID: NN:rdpencomapi.IRDPSRAPIInvitationManager
title: IRDPSRAPIInvitationManager
author: windows-sdk-content
description: Manages invitation objects.
old-location: rdp\irdpsrapiinvitationmanager.htm
tech.root: rdp
ms.assetid: 300940ef-e8a6-4dd9-a078-d4325e20ae91
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IRDPSRAPIInvitationManager, IRDPSRAPIInvitationManager interface [RDP], IRDPSRAPIInvitationManager interface [RDP],described, rdp.irdpsrapiinvitationmanager, rdpencomapi/IRDPSRAPIInvitationManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIInvitationManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPIInvitationManager interface


## -description


Manages invitation objects.

Applications obtain access to this object using <a href="https://msdn.microsoft.com/6e5116d9-7b65-4d93-ab1e-caac080e870e">IRDPSRAPISharingSession::get_Invitations</a>


This interface provides access to the <b>RDPSRAPIInvitationManager</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIInvitationManager</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IRDPSRAPIInvitationManager</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/169d220b-3a2a-490e-9c1c-03a707d59f6c">CreateInvitation</a>
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

<a href="https://msdn.microsoft.com/e1959226-04a0-4eae-9abb-b82cdd545975">_NewEnum</a>


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

<a href="https://msdn.microsoft.com/5b421537-ce9f-42d3-83b8-f051631c78de">Count</a>


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

<a href="https://msdn.microsoft.com/0a6acaec-0051-4753-8926-c708e75c3e07">Item</a>


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




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/66cd8251-726a-4368-8da5-4d3f6899bdc8">IRDPSRAPIInvitation</a>
 

 

