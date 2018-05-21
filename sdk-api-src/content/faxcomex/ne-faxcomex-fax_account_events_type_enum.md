---
UID: NE:faxcomex.FAX_ACCOUNT_EVENTS_TYPE_ENUM
title: FAX_ACCOUNT_EVENTS_TYPE_ENUM
author: windows-driver-content
description: Specifies the types of event notifications, on a particular account, that the server sends to listening clients.
old-location: fax\_mfax_fax_account_events_type_enum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\e\faxinto_z_fax_account_events_type_enum.htm
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: FAX_ACCOUNT_EVENTS_TYPE_ENUM, FAX_ACCOUNT_EVENTS_TYPE_ENUM enumeration [Fax Service], _mfax_fax_account_events_type_enum, faetFXSSVC_ENDED, faetIN_ARCHIVE, faetIN_QUEUE, faetNONE, faetOUT_ARCHIVE, faetOUT_QUEUE, fax._mfax_fax_account_events_type_enum, faxcomex/FAX_ACCOUNT_EVENTS_TYPE_ENUM, faxcomex/faetFXSSVC_ENDED, faxcomex/faetIN_ARCHIVE, faxcomex/faetIN_QUEUE, faxcomex/faetNONE, faxcomex/faetOUT_ARCHIVE, faxcomex/faetOUT_QUEUE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FAX_ACCOUNT_EVENTS_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	FaxComex.h
api_name:
-	FAX_ACCOUNT_EVENTS_TYPE_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
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
 





