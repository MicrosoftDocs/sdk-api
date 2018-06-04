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

# _ACTION_HEADER structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/library/windows/hardware/dn965731">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

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
 

 

