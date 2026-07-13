---
UID: NE:faxcomex.FAX_ACCOUNT_EVENTS_TYPE_ENUM
title: FAX_ACCOUNT_EVENTS_TYPE_ENUM (faxcomex.h)
description: Specifies the types of event notifications, on a particular account, that the server sends to listening clients.
helpviewer_keywords: ["FAX_ACCOUNT_EVENTS_TYPE_ENUM","FAX_ACCOUNT_EVENTS_TYPE_ENUM enumeration [Fax Service]","_mfax_fax_account_events_type_enum","faetFXSSVC_ENDED","faetIN_ARCHIVE","faetIN_QUEUE","faetNONE","faetOUT_ARCHIVE","faetOUT_QUEUE","fax._mfax_fax_account_events_type_enum","faxcomex/FAX_ACCOUNT_EVENTS_TYPE_ENUM","faxcomex/faetFXSSVC_ENDED","faxcomex/faetIN_ARCHIVE","faxcomex/faetIN_QUEUE","faxcomex/faetNONE","faxcomex/faetOUT_ARCHIVE","faxcomex/faetOUT_QUEUE"]
old-location: fax\_mfax_fax_account_events_type_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\e\faxinto_z_fax_account_events_type_enum.htm
ms.date: 12/05/2018
ms.keywords: FAX_ACCOUNT_EVENTS_TYPE_ENUM, FAX_ACCOUNT_EVENTS_TYPE_ENUM enumeration [Fax Service], _mfax_fax_account_events_type_enum, faetFXSSVC_ENDED, faetIN_ARCHIVE, faetIN_QUEUE, faetNONE, faetOUT_ARCHIVE, faetOUT_QUEUE, fax._mfax_fax_account_events_type_enum, faxcomex/FAX_ACCOUNT_EVENTS_TYPE_ENUM, faxcomex/faetFXSSVC_ENDED, faxcomex/faetIN_ARCHIVE, faxcomex/faetIN_QUEUE, faxcomex/faetNONE, faxcomex/faetOUT_ARCHIVE, faxcomex/faetOUT_QUEUE
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_ACCOUNT_EVENTS_TYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_ACCOUNT_EVENTS_TYPE_ENUM
 - faxcomex/FAX_ACCOUNT_EVENTS_TYPE_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_ACCOUNT_EVENTS_TYPE_ENUM
---

# FAX_ACCOUNT_EVENTS_TYPE_ENUM enumeration


## -description

Specifies the types of event notifications, on a particular account, that the server sends to listening clients.

## -enum-fields

### -field faetNONE:0

No notifications are sent.

### -field faetIN_QUEUE:0x1

Notifications of changes to the state of any fax in the incoming queue are sent.

### -field faetOUT_QUEUE:0x2

Notifications of changes to the state of any fax in the outgoing queue are sent.

### -field faetIN_ARCHIVE:0x4

A notification is sent whenever a message is removed from the incoming fax archive.

### -field faetOUT_ARCHIVE:0x8

A notification is sent whenever a message is removed from the outgoing fax archive.

### -field faetFXSSVC_ENDED:0x10

A notification is sent whenever the fax service stops executing.

## -remarks

The following table lists the <a href="/windows/win32/api/faxcomex/nn-faxcomex-_ifaxaccountnotify">IFaxAccountNotify</a> methods called by each member of the enumeration:


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
<td>OnIncomingJobAdded</p>OnIncomingJobRemoved</p>OnIncomingJobChanged</td>
</tr>
<tr>
<td>faetOUT_QUEUE</td>
<td>OnOutgoingJobAdded</p>OnOutgoingJobRemoved</p>OnOutgoingJobChanged</td>
</tr>
<tr>
<td>faetIN_ARCHIVE</td>
<td>OnIncomingMessageAdded</p>OnIncomingMessageRemoved</td>
</tr>
<tr>
<td>faetOUT_ARCHIVE</td>
<td>OnOutgoingMessageAdded</p>OnOutgoingMessageRemoved</td>
</tr>
<tr>
<td>faetFXSSVC_ENDED</td>
<td>OnServerShutDown</td>
</tr>
</table>

