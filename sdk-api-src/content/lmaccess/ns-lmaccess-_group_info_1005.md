---
UID: NS:lmaccess._GROUP_INFO_1005
title: "_GROUP_INFO_1005"
author: windows-sdk-content
description: The GROUP_INFO_1005 structure contains the resource attributes associated with a global group.
old-location: netmgmt\group_info_1005_str.htm
tech.root: netmgmt
ms.assetid: bd93820a-e019-45f4-88c7-011a517955ad
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*LPGROUP_INFO_1005, *PGROUP_INFO_1005, GROUP_INFO_1005, GROUP_INFO_1005 structure [Network Management], LPGROUP_INFO_1005, LPGROUP_INFO_1005 structure pointer [Network Management], PGROUP_INFO_1005, PGROUP_INFO_1005 structure pointer [Network Management], _GROUP_INFO_1005, _win32_group_info_1005_str, lmaccess/GROUP_INFO_1005, lmaccess/LPGROUP_INFO_1005, lmaccess/PGROUP_INFO_1005, netmgmt.group_info_1005_str"
ms.prod: windows
ms.technology: windows-sdk
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
 - GROUP_INFO_1005
product: Windows
targetos: Windows
req.typenames: GROUP_INFO_1005, *PGROUP_INFO_1005, *LPGROUP_INFO_1005
req.redist: 
---

# _GROUP_INFO_1005 structure


## -description


The
				<b>GROUP_INFO_1005</b> structure contains the resource attributes associated with a global group.


## -struct-fields




### -field grpi1005_attributes

These attributes are hard-coded to SE_GROUP_MANDATORY, SE_GROUP_ENABLED, and SE_GROUP_ENABLED_BY_DEFAULT. For more information, see 
<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a>. 



					


## -see-also




<a href="https://msdn.microsoft.com/2199258d-bde9-4fdb-b9c1-147616420fbe">Group Functions</a>



<a href="https://msdn.microsoft.com/8c235f9a-095e-4108-9b93-008ffe9bc776">NetGroupSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a>
 

 

