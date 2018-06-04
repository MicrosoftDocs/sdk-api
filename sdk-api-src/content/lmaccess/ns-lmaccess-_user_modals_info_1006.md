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

# _USER_MODALS_INFO_1006 structure


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
 

 

