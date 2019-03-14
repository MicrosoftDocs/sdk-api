---
UID: NS:lmaccess._USER_MODALS_INFO_1006
title: USER_MODALS_INFO_1006
author: windows-sdk-content
description: The USER_MODALS_INFO_1006 structure contains logon server information.
old-location: netmgmt\user_modals_info_1006_str.htm
tech.root: NetMgmt
ms.assetid: ca5c0819-b4a0-4d07-90fc-54c86ac5ecf5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPUSER_MODALS_INFO_1006, *PUSER_MODALS_INFO_1006, LPUSER_MODALS_INFO_1006, LPUSER_MODALS_INFO_1006 structure pointer [Network Management], PUSER_MODALS_INFO_1006, PUSER_MODALS_INFO_1006 structure pointer [Network Management], UAS_ROLE_BACKUP, UAS_ROLE_MEMBER, UAS_ROLE_PRIMARY, UAS_ROLE_STANDALONE, USER_MODALS_INFO_1006, USER_MODALS_INFO_1006 structure [Network Management], _win32_user_modals_info_1006_str, lmaccess/LPUSER_MODALS_INFO_1006, lmaccess/PUSER_MODALS_INFO_1006, lmaccess/USER_MODALS_INFO_1006, netmgmt.user_modals_info_1006_str"
ms.topic: struct
req.header: lmaccess.h
req.include-header: Lm.h
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
 - Lmaccess.h
api_name:
 - USER_MODALS_INFO_1006
product: Windows
targetos: Windows
req.typenames: USER_MODALS_INFO_1006, *PUSER_MODALS_INFO_1006, *LPUSER_MODALS_INFO_1006
req.redist: 
---

# USER_MODALS_INFO_1006 structure


## -description


The 
				<b>USER_MODALS_INFO_1006</b> structure contains logon server information.


## -struct-fields




### -field usrmod1006_role

Specifies the role of the logon server. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UAS_ROLE_STANDALONE"></a><a id="uas_role_standalone"></a><dl>
<dt><b>UAS_ROLE_STANDALONE</b></dt>
</dl>
</td>
<td width="60%">
Logon server is a stand-alone. Use this value if no logon services are available.

</td>
</tr>
<tr>
<td width="40%"><a id="UAS_ROLE_MEMBER"></a><a id="uas_role_member"></a><dl>
<dt><b>UAS_ROLE_MEMBER</b></dt>
</dl>
</td>
<td width="60%">
Logon server is a member.

</td>
</tr>
<tr>
<td width="40%"><a id="UAS_ROLE_BACKUP"></a><a id="uas_role_backup"></a><dl>
<dt><b>UAS_ROLE_BACKUP</b></dt>
</dl>
</td>
<td width="60%">
Logon server is a backup.

</td>
</tr>
<tr>
<td width="40%"><a id="UAS_ROLE_PRIMARY"></a><a id="uas_role_primary"></a><dl>
<dt><b>UAS_ROLE_PRIMARY</b></dt>
</dl>
</td>
<td width="60%">
Logon server is a domain controller.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/9884e076-ee6a-4aca-abe6-a79754667759">NetUserModalsSet</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/e655b9f6-2808-4bd4-998c-c8a2e980920b">User Modal Functions</a>
 

 

