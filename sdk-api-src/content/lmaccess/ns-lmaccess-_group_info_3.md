---
UID: NS:lmaccess._GROUP_INFO_3
title: "_GROUP_INFO_3"
author: windows-sdk-content
description: The GROUP_INFO_3 structure contains information about a global group, including name, security identifier (SID), and resource attributes.
old-location: netmgmt\group_info_3_str.htm
tech.root: netmgmt
ms.assetid: aa0c3b6e-ab27-48b9-a37f-5cceb63c70fd
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PGROUP_INFO_3, GROUP_INFO_3, GROUP_INFO_3 structure [Network Management], PGROUP_INFO_3, PGROUP_INFO_3 structure pointer [Network Management], _GROUP_INFO_3, _win32_group_info_3_str, lmaccess/GROUP_INFO_3, lmaccess/PGROUP_INFO_3, netmgmt.group_info_3_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - GROUP_INFO_3
product: Windows
targetos: Windows
req.typenames: GROUP_INFO_3, *PGROUP_INFO_3
req.redist: 
---

# _GROUP_INFO_3 structure


## -description


The
				<b>GROUP_INFO_3</b> structure contains information about a global group, including name, security identifier (SID), and resource attributes.


## -struct-fields




### -field grpi3_name

Pointer to a null-terminated Unicode character string that specifies the name of the global group. 




When you call the 
<a href="https://msdn.microsoft.com/8c235f9a-095e-4108-9b93-008ffe9bc776">NetGroupSetInfo</a> function this member is ignored.


### -field grpi3_comment

Pointer to a null-terminated Unicode character string that contains a remark associated with the global group. This member can be a null string. The comment can contain MAXCOMMENTSZ characters.


### -field grpi3_group_sid

Pointer to a 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that contains the 
<a href="security.security_identifiers_sids_">security identifier (SID)</a> that uniquely identifies the global group. The 
<a href="https://msdn.microsoft.com/b5ca5f76-d40b-4abf-925a-0de54fc476e4">NetUserAdd</a> and 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> functions ignore this member.


### -field grpi3_attributes

These attributes are hard-coded to SE_GROUP_MANDATORY, SE_GROUP_ENABLED, and SE_GROUP_ENABLED_BY_DEFAULT. For more information, see 
<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a>.
					


## -see-also




<a href="https://msdn.microsoft.com/2199258d-bde9-4fdb-b9c1-147616420fbe">Group Functions</a>



<a href="https://msdn.microsoft.com/fbf90758-79fd-4959-b6d0-ad3872e77242">NetGroupAdd</a>



<a href="https://msdn.microsoft.com/3f8fabce-94cb-41f5-9af1-04585ac3f16e">NetGroupEnum</a>



<a href="https://msdn.microsoft.com/f9957c15-9a49-4b53-ae31-efd6a03417a6">NetGroupGetInfo</a>



<a href="https://msdn.microsoft.com/8c235f9a-095e-4108-9b93-008ffe9bc776">NetGroupSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a>
 

 

