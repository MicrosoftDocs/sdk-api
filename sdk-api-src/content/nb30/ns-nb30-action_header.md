---
UID: NS:nb30._ACTION_HEADER
title: ACTION_HEADER
author: windows-sdk-content
description: The ACTION_HEADER structure contains information about an action. This action is an extension to the standard transport interface.
old-location: netbios\action_header.htm
tech.root: NetBIOS
ms.assetid: f2bbf394-972a-4e96-8cc6-9f230359cbfc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PACTION_HEADER, ACTION_HEADER, ACTION_HEADER structure [NetBIOS], MABF, MNBF, MOOO, MXNS, PACTION_HEADER, PACTION_HEADER structure pointer [NetBIOS], nb30/ACTION_HEADER, nb30/PACTION_HEADER, netbios.action_header"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nb30.h
api_name:
 - ACTION_HEADER
product: Windows
targetos: Windows
req.typenames: ACTION_HEADER, *PACTION_HEADER
req.redist: 
---

# ACTION_HEADER structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/9144e283-0e5f-43d7-8cd2-e746f94c6f14">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

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



The scope of the action is determined by the <b>ncb_lsn</b> and <b>ncb_num</b> members of the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure, as follows.

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



<a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a>



<a href="https://msdn.microsoft.com/64ef39ec-d69a-4e33-9192-dda6d1bb84b8">NetBIOS Structures</a>



<a href="https://msdn.microsoft.com/9144e283-0e5f-43d7-8cd2-e746f94c6f14">The NetBIOS Interface Overview</a>
 

 

