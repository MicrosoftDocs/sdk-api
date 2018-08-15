---
UID: NS:lmaccess._GROUP_INFO_1002
title: "_GROUP_INFO_1002"
author: windows-sdk-content
description: The GROUP_INFO_1002 structure contains a comment to associate with a global group.
old-location: netmgmt\group_info_1002_str.htm
old-project: netmgmt
ms.assetid: 9c322ef5-4f98-44ad-8b57-40f8533eb9c1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPGROUP_INFO_1002, *PGROUP_INFO_1002, GROUP_INFO_1002, GROUP_INFO_1002 structure [Network Management], LPGROUP_INFO_1002, LPGROUP_INFO_1002 structure pointer [Network Management], PGROUP_INFO_1002, PGROUP_INFO_1002 structure pointer [Network Management], _GROUP_INFO_1002, _win32_group_info_1002_str, lmaccess/GROUP_INFO_1002, lmaccess/LPGROUP_INFO_1002, lmaccess/PGROUP_INFO_1002, netmgmt.group_info_1002_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmaccess.h
req.include-header: Lm.h
req.redist: 
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
tech.root: 
req.typenames: GROUP_INFO_1002, *PGROUP_INFO_1002, *LPGROUP_INFO_1002
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - GROUP_INFO_1002
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _GROUP_INFO_1002 structure


## -description


The
				<b>GROUP_INFO_1002</b> structure contains a comment to associate with a global group.


## -struct-fields




### -field grpi1002_comment

Pointer to a null-terminated Unicode character string that contains a remark to associate with the global group. This member can be a null string. The comment can contain MAXCOMMENTSZ characters.


## -see-also




<a href="https://msdn.microsoft.com/2199258d-bde9-4fdb-b9c1-147616420fbe">Group Functions</a>



<a href="https://msdn.microsoft.com/8c235f9a-095e-4108-9b93-008ffe9bc776">NetGroupSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

