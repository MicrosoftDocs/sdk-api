---
UID: NS:lmaccess._LOCALGROUP_MEMBERS_INFO_0
title: "_LOCALGROUP_MEMBERS_INFO_0"
author: windows-sdk-content
description: The LOCALGROUP_MEMBERS_INFO_0 structure contains the security identifier (SID) associated with a local group member. The member can be a user account or a global group account.
old-location: netmgmt\localgroup_members_info_0_str.htm
tech.root: NetMgmt
ms.assetid: e559cd90-942c-442a-b57f-7d2024523455
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPLOCALGROUP_MEMBERS_INFO_0, *PLOCALGROUP_MEMBERS_INFO_0, LOCALGROUP_MEMBERS_INFO_0, LOCALGROUP_MEMBERS_INFO_0 structure [Network Management], _LOCALGROUP_MEMBERS_INFO_0, _win32_localgroup_members_info_0_str, lmaccess/LOCALGROUP_MEMBERS_INFO_0, netmgmt.localgroup_members_info_0_str"
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
 - LOCALGROUP_MEMBERS_INFO_0
product: Windows
targetos: Windows
req.typenames: LOCALGROUP_MEMBERS_INFO_0, *PLOCALGROUP_MEMBERS_INFO_0, *LPLOCALGROUP_MEMBERS_INFO_0
req.redist: 
---

# _LOCALGROUP_MEMBERS_INFO_0 structure


## -description


The 
				<b>LOCALGROUP_MEMBERS_INFO_0</b> structure contains the security identifier (SID) associated with a local group member. The member can be a user account or a global group account.


## -struct-fields




### -field lgrmi0_sid

Pointer to a 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that contains the 
<a href="security.security_identifiers_sids_">security identifier (SID)</a> of the local group member.


## -see-also




<a href="https://msdn.microsoft.com/d6b1b729-cdd5-4ed3-a5a1-cf3a8b6cecf2">LOCALGROUP_MEMBERS_INFO_1</a>



<a href="https://msdn.microsoft.com/f5cd6e84-1111-4558-bec4-26af13f21b61">LOCALGROUP_MEMBERS_INFO_2</a>



<a href="https://msdn.microsoft.com/e8d1d884-c955-4706-bc3e-142469b02545">LOCALGROUP_MEMBERS_INFO_3</a>



<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group Functions</a>



<a href="https://msdn.microsoft.com/3b2d3e4a-742e-4e67-8b28-3cd6d7e6a857">NetLocalGroupAddMembers</a>



<a href="https://msdn.microsoft.com/85ae796b-c94a-46a8-9fa8-6c612db38671">NetLocalGroupDelMembers</a>



<a href="https://msdn.microsoft.com/35770b32-dae9-46f5-84e3-1c31ca22f708">NetLocalGroupGetMembers</a>



<a href="https://msdn.microsoft.com/4dce1e10-b74d-4d69-ac5a-12e7d9d84e5c">NetLocalGroupSetMembers</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

