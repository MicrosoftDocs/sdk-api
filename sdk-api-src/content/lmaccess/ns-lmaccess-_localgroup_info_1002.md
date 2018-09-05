---
UID: NS:lmaccess._LOCALGROUP_INFO_1002
title: "_LOCALGROUP_INFO_1002"
author: windows-sdk-content
description: The LOCALGROUP_INFO_1002 structure contains a comment describing a local group.
old-location: netmgmt\localgroup_info_1002_str.htm
old-project: netmgmt
ms.assetid: 027db4a3-6722-46e8-a204-922ed97cb3f5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPLOCALGROUP_INFO_1002, *PLOCALGROUP_INFO_1002, LOCALGROUP_INFO_1002, LOCALGROUP_INFO_1002 structure [Network Management], LPLOCALGROUP_INFO_1002, LPLOCALGROUP_INFO_1002 structure pointer [Network Management], PLOCALGROUP_INFO_1002, PLOCALGROUP_INFO_1002 structure pointer [Network Management], _LOCALGROUP_INFO_1002, _win32_localgroup_info_1002_str, lmaccess/LOCALGROUP_INFO_1002, lmaccess/LPLOCALGROUP_INFO_1002, lmaccess/PLOCALGROUP_INFO_1002, netmgmt.localgroup_info_1002_str"
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
req.typenames: LOCALGROUP_INFO_1002, *PLOCALGROUP_INFO_1002, *LPLOCALGROUP_INFO_1002
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - LOCALGROUP_INFO_1002
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _LOCALGROUP_INFO_1002 structure


## -description


The 
				<b>LOCALGROUP_INFO_1002</b> structure contains a comment describing a local group.


## -struct-fields




### -field lgrpi1002_comment

Pointer to a Unicode string that specifies a remark associated with the local group. This member can be a null string. The comment can have as many as MAXCOMMENTSZ characters.


## -see-also




<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group Functions</a>



<a href="https://msdn.microsoft.com/c1d2a68b-0910-4815-9547-0f0f3c983164">NetLocalGroupSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

