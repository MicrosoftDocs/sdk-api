---
UID: NS:lmaccess._LOCALGROUP_INFO_1002
title: LOCALGROUP_INFO_1002 (lmaccess.h)
author: windows-sdk-content
description: The LOCALGROUP_INFO_1002 structure contains a comment describing a local group.
old-location: netmgmt\localgroup_info_1002_str.htm
tech.root: NetMgmt
ms.assetid: 027db4a3-6722-46e8-a204-922ed97cb3f5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLOCALGROUP_INFO_1002, *PLOCALGROUP_INFO_1002, LOCALGROUP_INFO_1002, LOCALGROUP_INFO_1002 structure [Network Management], LPLOCALGROUP_INFO_1002, LPLOCALGROUP_INFO_1002 structure pointer [Network Management], PLOCALGROUP_INFO_1002, PLOCALGROUP_INFO_1002 structure pointer [Network Management], _win32_localgroup_info_1002_str, lmaccess/LOCALGROUP_INFO_1002, lmaccess/LPLOCALGROUP_INFO_1002, lmaccess/PLOCALGROUP_INFO_1002, netmgmt.localgroup_info_1002_str"
ms.topic: struct
f1_keywords: 
 - "lmaccess/LOCALGROUP_INFO_1002"
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
 - LOCALGROUP_INFO_1002
targetos: Windows
req.typenames: LOCALGROUP_INFO_1002, *PLOCALGROUP_INFO_1002, *LPLOCALGROUP_INFO_1002
req.redist: 
ms.custom: 19H1
---

# LOCALGROUP_INFO_1002 structure


## -description


The 
				<b>LOCALGROUP_INFO_1002</b> structure contains a comment describing a local group.


## -struct-fields




### -field lgrpi1002_comment

Pointer to a Unicode string that specifies a remark associated with the local group. This member can be a null string. The comment can have as many as MAXCOMMENTSZ characters.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/local-group-functions">Local Group Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupsetinfo">NetLocalGroupSetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>
 

 

