---
UID: NS:lmaccess._USER_MODALS_INFO_1
title: "_USER_MODALS_INFO_1"
author: windows-sdk-content
description: The USER_MODALS_INFO_1 structure contains logon server and domain controller information.
old-location: netmgmt\user_modals_info_1_str.htm
tech.root: netmgmt
ms.assetid: 2cb7f310-c76e-42fd-892c-fead374af16c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*LPUSER_MODALS_INFO_1, *PUSER_MODALS_INFO_1, LPUSER_MODALS_INFO_1, LPUSER_MODALS_INFO_1 structure pointer [Network Management], PUSER_MODALS_INFO_1, PUSER_MODALS_INFO_1 structure pointer [Network Management], UAS_ROLE_BACKUP, UAS_ROLE_MEMBER, UAS_ROLE_PRIMARY, UAS_ROLE_STANDALONE, USER_MODALS_INFO_1, USER_MODALS_INFO_1 structure [Network Management], _USER_MODALS_INFO_1, _win32_user_modals_info_1_str, lmaccess/LPUSER_MODALS_INFO_1, lmaccess/PUSER_MODALS_INFO_1, lmaccess/USER_MODALS_INFO_1, netmgmt.user_modals_info_1_str"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - USER_MODALS_INFO_1
product: Windows
targetos: Windows
req.typenames: USER_MODALS_INFO_1, *PUSER_MODALS_INFO_1, *LPUSER_MODALS_INFO_1
req.redist: 
---

# _USER_MODALS_INFO_1 structure


## -description


The
				<b>USER_MODALS_INFO_1</b> structure contains logon server and domain controller information.


## -struct-fields




### -field usrmod1_role

Specifies the role of the logon server. The following values are defined. 



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
The logon server is a stand-alone server.

</td>
</tr>
<tr>
<td width="40%"><a id="UAS_ROLE_MEMBER"></a><a id="uas_role_member"></a><dl>
<dt><b>UAS_ROLE_MEMBER</b></dt>
</dl>
</td>
<td width="60%">
The logon server is a member.

</td>
</tr>
<tr>
<td width="40%"><a id="UAS_ROLE_BACKUP"></a><a id="uas_role_backup"></a><dl>
<dt><b>UAS_ROLE_BACKUP</b></dt>
</dl>
</td>
<td width="60%">
The logon server is a backup.

</td>
</tr>
<tr>
<td width="40%"><a id="UAS_ROLE_PRIMARY"></a><a id="uas_role_primary"></a><dl>
<dt><b>UAS_ROLE_PRIMARY</b></dt>
</dl>
</td>
<td width="60%">
The logon server is a domain controller.

</td>
</tr>
</table>
 


<div> </div>


If the Netlogon service is not being used, the element should be set to UAS_ROLE_STANDALONE.


### -field usrmod1_primary

Pointer to a Unicode string that specifies the name of the domain controller that stores the primary copy of the database for the user account manager.


## -see-also




<a href="https://msdn.microsoft.com/5bb18144-82a6-4e9b-8321-c06a667bdd03">NetUserModalsGet</a>



<a href="https://msdn.microsoft.com/9884e076-ee6a-4aca-abe6-a79754667759">NetUserModalsSet</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/e655b9f6-2808-4bd4-998c-c8a2e980920b">User Modal Functions</a>
 

 

