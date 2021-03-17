---
UID: NS:p2p.peer_record_tag
title: PEER_RECORD (p2p.h)
description: The PEER_RECORD structure contains the record object that an application uses.
helpviewer_keywords: ["*PPEER_RECORD","PEER_RECORD","PEER_RECORD structure [Peer Networking]","PPEER_RECORD","PPEER_RECORD structure pointer [Peer Networking]","p2p.peer_record","p2p/PPEER_RECORD","p2p/peer_record_tag"]
old-location: p2p\peer_record.htm
tech.root: p2p
ms.assetid: 4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1
ms.date: 12/05/2018
ms.keywords: '*PPEER_RECORD, PEER_RECORD, PEER_RECORD structure [Peer Networking], PPEER_RECORD, PPEER_RECORD structure pointer [Peer Networking], p2p.peer_record, p2p/PPEER_RECORD, p2p/peer_record_tag'
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
req.target-min-winversvr: None supported
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
req.typenames: PEER_RECORD, *PPEER_RECORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_record_tag
 - p2p/peer_record_tag
 - PPEER_RECORD
 - p2p/PPEER_RECORD
 - PEER_RECORD
 - p2p/PEER_RECORD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_RECORD
---

# PEER_RECORD structure


## -description

The <b>PEER_RECORD</b> structure contains the record object that an application uses.

## -struct-fields

### -field dwSize

Specifies the size of a structure.  Set the value to   sizeof(<b>PEER_RECORD</b>).

### -field type

Specifies the type of  record. The  type is a <b>GUID</b> that an application must specify.  The <b>GUID</b> represents a unique record type, for example, a chat record.

### -field id

Specifies the unique ID of a record. The Peer Infrastructure supplies this ID. This parameter is ignored in calls to  <a href="/windows/desktop/api/p2p/nf-p2p-peergroupaddrecord">PeerGroupAddRecord</a>. An application cannot modify this member.

### -field dwVersion

Specifies the version of a record that   the Peer Infrastructure supplies when an application  calls <a href="/windows/desktop/api/p2p/nf-p2p-peergraphaddrecord">PeerGraphAddRecord</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphupdaterecord">PeerGraphUpdateRecord</a>. An application cannot modify this member.

### -field dwFlags

Specifies the flags that indicate  special processing, which must be applied to  a record.  The following table identifies the valid values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>PEER_RECORD_FLAG_AUTOREFRESH</b></td>
<td>Indicates that a record is automatically refreshed when it is ready to expire.	</td>
</tr>
<tr>
<td><b>PEER_RECORD_FLAG_DELETED</b></td>
<td>Indicates that a record is marked as deleted. </td>
</tr>
</table>
 

<div class="alert"><b>Note</b>   An application cannot set these flags.</div>
<div> </div>

### -field pwzCreatorId

Pointer to the unique ID of a record creator.   This member is set to <b>NULL</b> for calls to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphaddrecord">PeerGraphAddRecord</a> and <a href="/windows/desktop/api/p2p/nf-p2p-peergraphupdaterecord">PeerGraphUpdateRecord</a>. An application cannot set this member.

### -field pwzModifiedById

Specifies the unique ID of  the last person who changes a record. An application cannot set this member.

### -field pwzAttributes

Pointer to the set of attribute name and value pairs that are   associated with a record. This member points to   an XML string. Record attributes are specified as an XML string,  and they must be consistent with the Peer Infrastructure record attribute schema.   For a complete explanation of the XML schema, see <a href="/windows/desktop/P2PSdk/record-attribute-schema">Record Attribute Schema</a>.

The Peer Infrastructure reserves several attribute names that a user cannot set. The following list identifies the reserved attribute names:<ul>
<li><b>peerlastmodifiedby</b></li>
<li><b>peercreatorid</b></li>
<li><b>peerlastmodificationtime</b></li>
<li><b>peerrecordid</b></li>
<li><b>peerrecordtype</b></li>
<li><b>peercreationtime</b></li>
<li><b>peerlastmodificationtime</b></li>
</ul>

### -field ftCreation

Specifies the Coordinated Universal Time (UTC) that a record is created. The Peer Infrastructure supplies this value, and the value is set to zero (0) in calls to <a href="/windows/desktop/api/p2p/nf-p2p-peergroupaddrecord">PeerGroupAddRecord</a>. An application cannot set this member.

### -field ftExpiration

The UTC time that a record expires. This member is required.  It can be updated to a time value greater than the originally specified time value, but  it cannot be less than the  originally specified value.

<div class="alert"><b>Note</b>   If <b>dwFlags</b> is set to <b>PEER_RECORD_FLAG_AUTOREFRESH</b>, do not set the value  of   <b>ftExpiration</b> to less than four (4) minutes. If this member is set to less than four (4) minutes, undefined behavior can occur.</div>
<div> </div>

### -field ftLastModified

The UTC time that a record is modified.   The Peer Infrastructure supplies this value. Set this member to  <b>NULL</b> when  calling  <a href="/windows/desktop/api/p2p/nf-p2p-peergraphaddrecord">PeerGraphAddRecord</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergraphupdaterecord">PeerGraphUpdateRecord</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupaddrecord">PeerGroupAddRecord</a>, and <a href="/windows/desktop/api/p2p/nf-p2p-peergroupupdaterecord">PeerGroupUpdateRecord</a>. An application cannot set this member.

### -field securityData

Specifies the security data contained in a  <a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a> structure. The Graphing API uses this member, and provides  the security provider with a place to store security data, for example, a signature.  The Grouping API cannot modify this member.

### -field data

Specifies the actual data that this record contains.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a>



<a href="/windows/desktop/api/p2p/nc-p2p-pfnpeer_secure_record">PFNPEER_SECURE_RECORD</a>



<a href="/windows/desktop/api/p2p/nc-p2p-pfnpeer_validate_record">PFNPEER_VALIDATE_RECORD</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphaddrecord">PeerGraphAddRecord</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphdeleterecord">PeerGraphDeleteRecord</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetrecord">PeerGraphGetRecord</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphupdaterecord">PeerGraphUpdateRecord</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupaddrecord">PeerGroupAddRecord</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupdeleterecord">PeerGroupDeleteRecord</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupgetrecord">PeerGroupGetRecord</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupupdaterecord">PeerGroupUpdateRecord</a>