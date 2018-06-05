---
UID: NS:lmaccess._LOCALGROUP_INFO_1
title: "_LOCALGROUP_INFO_1"
author: windows-sdk-content
description: The LOCALGROUP_INFO_1 structure contains a local group name and a comment describing the local group.
old-location: netmgmt\localgroup_info_1_str.htm
old-project: NetMgmt
ms.assetid: b96d7ddc-3ffb-4203-88b1-4aa123051695
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPLOCALGROUP_INFO_1, *PLOCALGROUP_INFO_1, LOCALGROUP_INFO_1, LOCALGROUP_INFO_1 structure [Network Management], LPLOCALGROUP_INFO_1, LPLOCALGROUP_INFO_1 structure pointer [Network Management], PLOCALGROUP_INFO_1, PLOCALGROUP_INFO_1 structure pointer [Network Management], _LOCALGROUP_INFO_1, _win32_localgroup_info_1_str, lmaccess/LOCALGROUP_INFO_1, lmaccess/LPLOCALGROUP_INFO_1, lmaccess/PLOCALGROUP_INFO_1, netmgmt.localgroup_info_1_str"
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
tech.root: 
req.typenames: LOCALGROUP_INFO_1, *PLOCALGROUP_INFO_1, *LPLOCALGROUP_INFO_1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmaccess.h
api_name:
-	LOCALGROUP_INFO_1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _LOCALGROUP_INFO_1 structure


## -description


The
				<b>LOCALGROUP_INFO_1</b> structure contains a local group name and a comment describing the local group.


## -struct-fields




### -field lgrpi1_name

Pointer to a Unicode string that specifies a local group name. For more information, see the following Remarks section. 




This member is ignored when you call the 
<a href="https://msdn.microsoft.com/c1d2a68b-0910-4815-9547-0f0f3c983164">NetLocalGroupSetInfo</a> function.


### -field lgrpi1_comment

Pointer to a Unicode string that contains a remark associated with the local group. This member can be a null string. The comment can have as many as MAXCOMMENTSZ characters.


## -remarks



User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group Functions</a>



<a href="https://msdn.microsoft.com/5028c1bc-8fed-4f02-8e69-d0d122b08d9f">NetLocalGroupAdd</a>



<a href="https://msdn.microsoft.com/fc27d7f1-bfbe-46d7-a154-f04eb9249248">NetLocalGroupEnum</a>



<a href="https://msdn.microsoft.com/ee2f0be9-8d52-439b-ab65-f9e11a2872c5">NetLocalGroupGetInfo</a>



<a href="https://msdn.microsoft.com/c1d2a68b-0910-4815-9547-0f0f3c983164">NetLocalGroupSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

