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

# _LOCALGROUP_MEMBERS_INFO_0 structure


## -description


The 
				<b>LOCALGROUP_MEMBERS_INFO_0</b> structure contains the security identifier (SID) associated with a local group member. The member can be a user account or a global group account.


## -struct-fields




### -field lgrmi0_sid

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure that contains the 
<a href="security.security_identifiers_sids_">security identifier (SID)</a> of the local group member.


## -see-also




<a href="https://msdn.microsoft.com/d6b1b729-cdd5-4ed3-a5a1-cf3a8b6cecf2">LOCALGROUP_MEMBERS_INFO_1</a>



<a href="https://msdn.microsoft.com/f5cd6e84-1111-4558-bec4-26af13f21b61">
LOCALGROUP_MEMBERS_INFO_2</a>



<a href="https://msdn.microsoft.com/e8d1d884-c955-4706-bc3e-142469b02545">
LOCALGROUP_MEMBERS_INFO_3</a>



<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group Functions</a>



<a href="https://msdn.microsoft.com/3b2d3e4a-742e-4e67-8b28-3cd6d7e6a857">NetLocalGroupAddMembers</a>



<a href="https://msdn.microsoft.com/85ae796b-c94a-46a8-9fa8-6c612db38671">NetLocalGroupDelMembers</a>



<a href="https://msdn.microsoft.com/35770b32-dae9-46f5-84e3-1c31ca22f708">NetLocalGroupGetMembers</a>



<a href="https://msdn.microsoft.com/4dce1e10-b74d-4d69-ac5a-12e7d9d84e5c">NetLocalGroupSetMembers</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

