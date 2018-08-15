---
UID: NS:lmaccess._LOCALGROUP_INFO_0
title: "_LOCALGROUP_INFO_0"
author: windows-sdk-content
description: The LOCALGROUP_INFO_0 structure contains a local group name.
old-location: netmgmt\localgroup_info_0_str.htm
old-project: netmgmt
ms.assetid: dfdb4c20-ea4a-45c9-b4f3-d6a844f89bb6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPLOCALGROUP_INFO_0, *PLOCALGROUP_INFO_0, LOCALGROUP_INFO_0, LOCALGROUP_INFO_0 structure [Network Management], LPLOCALGROUP_INFO_0, LPLOCALGROUP_INFO_0 structure pointer [Network Management], PLOCALGROUP_INFO_0, PLOCALGROUP_INFO_0 structure pointer [Network Management], _LOCALGROUP_INFO_0, _win32_localgroup_info_0_str, lmaccess/LOCALGROUP_INFO_0, lmaccess/LPLOCALGROUP_INFO_0, lmaccess/PLOCALGROUP_INFO_0, netmgmt.localgroup_info_0_str"
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
req.typenames: LOCALGROUP_INFO_0, *PLOCALGROUP_INFO_0, *LPLOCALGROUP_INFO_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - LOCALGROUP_INFO_0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _LOCALGROUP_INFO_0 structure


## -description


The
				<b>LOCALGROUP_INFO_0</b> structure contains a local group name.


## -struct-fields




### -field lgrpi0_name

Pointer to a Unicode string that specifies a local group name. For more information, see the following Remarks section.


## -remarks



When you call the 
<a href="https://msdn.microsoft.com/5028c1bc-8fed-4f02-8e69-d0d122b08d9f">NetLocalGroupAdd</a> function, this member specifies the name of a new local group. When you call the 
<a href="https://msdn.microsoft.com/c1d2a68b-0910-4815-9547-0f0f3c983164">NetLocalGroupSetInfo</a> function, this member specifies the new name of an existing local group.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group Functions</a>



<a href="https://msdn.microsoft.com/5028c1bc-8fed-4f02-8e69-d0d122b08d9f">NetLocalGroupAdd</a>



<a href="https://msdn.microsoft.com/fc27d7f1-bfbe-46d7-a154-f04eb9249248">NetLocalGroupEnum</a>



<a href="https://msdn.microsoft.com/c1d2a68b-0910-4815-9547-0f0f3c983164">NetLocalGroupSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

