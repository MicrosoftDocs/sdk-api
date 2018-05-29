---
UID: NS:lmaccess._GROUP_INFO_1
title: "_GROUP_INFO_1"
author: windows-sdk-content
description: The GROUP_INFO_1 structure contains a global group name and a comment to associate with the group.
old-location: netmgmt\group_info_1_str.htm
old-project: NetMgmt
ms.assetid: 0b42a438-64fd-4f37-98b8-77e10c09548c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPGROUP_INFO_1, *PGROUP_INFO_1, GROUP_INFO_1, GROUP_INFO_1 structure [Network Management], LPGROUP_INFO_1, LPGROUP_INFO_1 structure pointer [Network Management], PGROUP_INFO_1, PGROUP_INFO_1 structure pointer [Network Management], _GROUP_INFO_1, _win32_group_info_1_str, lmaccess/GROUP_INFO_1, lmaccess/LPGROUP_INFO_1, lmaccess/PGROUP_INFO_1, netmgmt.group_info_1_str"
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
req.typenames: GROUP_INFO_1, *PGROUP_INFO_1, *LPGROUP_INFO_1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmaccess.h
api_name:
-	GROUP_INFO_1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _GROUP_INFO_1 structure


## -description


The
				<b>GROUP_INFO_1</b> structure contains a global group name and a comment to associate with the group.


## -struct-fields




### -field grpi1_name

Pointer to a null-terminated Unicode character string that specifies the name of the global group. For more information, see the following Remarks section. 




When you call the 
<a href="https://msdn.microsoft.com/8c235f9a-095e-4108-9b93-008ffe9bc776">NetGroupSetInfo</a> function this member is ignored.


### -field grpi1_comment

Pointer to a null-terminated Unicode character string that specifies a remark associated with the global group. This member can be a null string. The comment can contain MAXCOMMENTSZ characters.


## -remarks



User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://msdn.microsoft.com/2199258d-bde9-4fdb-b9c1-147616420fbe">Group Functions</a>



<a href="https://msdn.microsoft.com/fbf90758-79fd-4959-b6d0-ad3872e77242">NetGroupAdd</a>



<a href="https://msdn.microsoft.com/3f8fabce-94cb-41f5-9af1-04585ac3f16e">NetGroupEnum</a>



<a href="https://msdn.microsoft.com/f9957c15-9a49-4b53-ae31-efd6a03417a6">NetGroupGetInfo</a>



<a href="https://msdn.microsoft.com/8c235f9a-095e-4108-9b93-008ffe9bc776">NetGroupSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

