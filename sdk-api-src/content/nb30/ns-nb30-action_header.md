---
UID: NS:nb30._ACTION_HEADER
title: ACTION_HEADER (nb30.h)
description: The ACTION_HEADER structure contains information about an action. This action is an extension to the standard transport interface.
helpviewer_keywords: ["*PACTION_HEADER","ACTION_HEADER","ACTION_HEADER structure [NetBIOS]","MABF","MNBF","MOOO","MXNS","PACTION_HEADER","PACTION_HEADER structure pointer [NetBIOS]","nb30/ACTION_HEADER","nb30/PACTION_HEADER","netbios.action_header"]
old-location: netbios\action_header.htm
tech.root: NetBIOS
ms.assetid: f2bbf394-972a-4e96-8cc6-9f230359cbfc
ms.date: 12/05/2018
ms.keywords: '*PACTION_HEADER, ACTION_HEADER, ACTION_HEADER structure [NetBIOS], MABF, MNBF, MOOO, MXNS, PACTION_HEADER, PACTION_HEADER structure pointer [NetBIOS], nb30/ACTION_HEADER, nb30/PACTION_HEADER, netbios.action_header'
req.header: nb30.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: ACTION_HEADER, *PACTION_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACTION_HEADER
 - nb30/_ACTION_HEADER
 - PACTION_HEADER
 - nb30/PACTION_HEADER
 - ACTION_HEADER
 - nb30/ACTION_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nb30.h
api_name:
 - ACTION_HEADER
---

# ACTION_HEADER structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/netbios/portal">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The ACTION_HEADER structure contains information about an action. This action is an extension to the standard transport interface.

## -struct-fields

### -field transport_id

Specifies the transport provider. This member can be used to check the validity of the request by the transport.

This member is always a four-character string. All strings starting with the letter M are reserved, as shown in the following example.



#### MOOO (All transports)



#### MNBF (NBF)



#### MABF (AsyBEUI)



#### MXNS (XNS)

<b>Windows XP:  </b>Certain legacy networking protocols, including NetBEUI, will no longer be supported.

### -field action_code

Specifies the action.

### -field reserved

Reserved.

## -remarks

The scope of the action is determined by the <b>ncb_lsn</b> and <b>ncb_num</b> members of the <a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure, as follows.

<table>
<tr>
<th></th>
<th>ncb_lsn = 0</th>
<th>ncb_lsn != 0</th>
</tr>
<tr>
<td>ncb_num = 0</td>
<td>Action applies to control channel associated with the valid LAN adapter. </td>
<td>Action applies to connection identifier associated with the valid local session number. </td>
</tr>
<tr>
<td>ncb_num != 0</td>
<td>Action applies to address associated with the valid LAN adapter.</td>
<td>Illegal combination. </td>
</tr>
</table>

## -see-also

<b></b>



<a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a>



<a href="/previous-versions/windows/desktop/netbios/netbios-structures">NetBIOS Structures</a>



<a href="/previous-versions/windows/desktop/netbios/portal">The NetBIOS Interface Overview</a>