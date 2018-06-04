---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# FAX_ACCOUNT_EVENTS_TYPE_ENUM enumeration


## -description


Specifies the types of event notifications, on a particular account, that the server sends to listening clients.


## -enum-fields




### -field faetNONE

No notifications are sent.


### -field faetIN_QUEUE

Notifications of changes to the state of any fax in the incoming queue are sent.


### -field faetOUT_QUEUE

Notifications of changes to the state of any fax in the outgoing queue are sent.


### -field faetIN_ARCHIVE

A notification is sent whenever a message is removed from the incoming fax archive.


### -field faetOUT_ARCHIVE

A notification is sent whenever a message is removed from the outgoing fax archive.


### -field faetFXSSVC_ENDED

A notification is sent whenever the fax service stops executing.


## -remarks



The following table lists the <a href="https://msdn.microsoft.com/10867869-66bb-4e17-a9b3-7e943fe5f510">IFaxAccountNotify</a> methods called by each member of the enumeration:


<table class="clsStd">
<tr>
<th>Member</th>
<th>Methods Called</th>
</tr>
<tr>
<td>faetNONE</td>
<td>none</td>
</tr>
<tr>
<td>faetIN_QUEUE</td>
<td>OnIncomingJobAdded

			OnIncomingJobRemoved

			OnIncomingJobChanged</td>
</tr>
<tr>
<td>faetOUT_QUEUE</td>
<td>OnOutgoingJobAdded

			OnOutgoingJobRemoved

			OnOutgoingJobChanged</td>
</tr>
<tr>
<td>faetIN_ARCHIVE</td>
<td>OnIncomingMessageAdded

			OnIncomingMessageRemoved</td>
</tr>
<tr>
<td>faetOUT_ARCHIVE</td>
<td>OnOutgoingMessageAdded

			OnOutgoingMessageRemoved</td>
</tr>
<tr>
<td>faetFXSSVC_ENDED</td>
<td>OnServerShutDown</td>
</tr>
</table>
 





