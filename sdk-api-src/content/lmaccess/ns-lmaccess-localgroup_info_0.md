---
UID: NS:lmaccess._LOCALGROUP_INFO_0
title: LOCALGROUP_INFO_0 (lmaccess.h)
author: windows-sdk-content
description: The LOCALGROUP_INFO_0 structure contains a local group name.
old-location: netmgmt\localgroup_info_0_str.htm
tech.root: NetMgmt
ms.assetid: dfdb4c20-ea4a-45c9-b4f3-d6a844f89bb6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLOCALGROUP_INFO_0, *PLOCALGROUP_INFO_0, LOCALGROUP_INFO_0, LOCALGROUP_INFO_0 structure [Network Management], LPLOCALGROUP_INFO_0, LPLOCALGROUP_INFO_0 structure pointer [Network Management], PLOCALGROUP_INFO_0, PLOCALGROUP_INFO_0 structure pointer [Network Management], _win32_localgroup_info_0_str, lmaccess/LOCALGROUP_INFO_0, lmaccess/LPLOCALGROUP_INFO_0, lmaccess/PLOCALGROUP_INFO_0, netmgmt.localgroup_info_0_str"
ms.topic: struct
f1_keywords: 
 - "lmaccess/LOCALGROUP_INFO_0"
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
 - LOCALGROUP_INFO_0
product: Windows
targetos: Windows
req.typenames: LOCALGROUP_INFO_0, *PLOCALGROUP_INFO_0, *LPLOCALGROUP_INFO_0
req.redist: 
ms.custom: 19H1
---

# LOCALGROUP_INFO_0 structure


## -description


The
				<b>LOCALGROUP_INFO_0</b> structure contains a local group name.


## -struct-fields




### -field lgrpi0_name

Pointer to a Unicode string that specifies a local group name. For more information, see the following Remarks section.


## -remarks



When you call the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupadd">NetLocalGroupAdd</a> function, this member specifies the name of a new local group. When you call the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupsetinfo">NetLocalGroupSetInfo</a> function, this member specifies the new name of an existing local group.

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/local-group-functions">Local Group Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupadd">NetLocalGroupAdd</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupenum">NetLocalGroupEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupsetinfo">NetLocalGroupSetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>
 

 

