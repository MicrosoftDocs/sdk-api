---
UID: NS:lmaccess._LOCALGROUP_MEMBERS_INFO_0
title: LOCALGROUP_MEMBERS_INFO_0 (lmaccess.h)
author: windows-sdk-content
description: The LOCALGROUP_MEMBERS_INFO_0 structure contains the security identifier (SID) associated with a local group member. The member can be a user account or a global group account.
old-location: netmgmt\localgroup_members_info_0_str.htm
tech.root: NetMgmt
ms.assetid: e559cd90-942c-442a-b57f-7d2024523455
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLOCALGROUP_MEMBERS_INFO_0, *PLOCALGROUP_MEMBERS_INFO_0, LOCALGROUP_MEMBERS_INFO_0, LOCALGROUP_MEMBERS_INFO_0 structure [Network Management], _win32_localgroup_members_info_0_str, lmaccess/LOCALGROUP_MEMBERS_INFO_0, netmgmt.localgroup_members_info_0_str"
ms.topic: struct
f1_keywords: ["lmaccess/LOCALGROUP_MEMBERS_INFO_0"]
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
ms.custom: 19H1
---

# LOCALGROUP_MEMBERS_INFO_0 structure


## -description


The 
				<b>LOCALGROUP_MEMBERS_INFO_0</b> structure contains the security identifier (SID) associated with a local group member. The member can be a user account or a global group account.


## -struct-fields




### -field lgrmi0_sid

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_sid">SID</a> structure that contains the 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-identifiers">security identifier (SID)</a> of the local group member.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-_localgroup_members_info_1">LOCALGROUP_MEMBERS_INFO_1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-_localgroup_members_info_2">LOCALGROUP_MEMBERS_INFO_2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/ns-lmaccess-_localgroup_members_info_3">LOCALGROUP_MEMBERS_INFO_3</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/local-group-functions">Local Group Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmembers">NetLocalGroupAddMembers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmembers">NetLocalGroupDelMembers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupgetmembers">NetLocalGroupGetMembers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupsetmembers">NetLocalGroupSetMembers</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>
 

 

