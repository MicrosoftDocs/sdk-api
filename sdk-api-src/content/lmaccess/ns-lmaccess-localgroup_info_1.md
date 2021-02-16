---
UID: NS:lmaccess._LOCALGROUP_INFO_1
title: LOCALGROUP_INFO_1 (lmaccess.h)
description: The LOCALGROUP_INFO_1 structure contains a local group name and a comment describing the local group.
helpviewer_keywords: ["*LPLOCALGROUP_INFO_1","*PLOCALGROUP_INFO_1","LOCALGROUP_INFO_1","LOCALGROUP_INFO_1 structure [Network Management]","LPLOCALGROUP_INFO_1","LPLOCALGROUP_INFO_1 structure pointer [Network Management]","PLOCALGROUP_INFO_1","PLOCALGROUP_INFO_1 structure pointer [Network Management]","_win32_localgroup_info_1_str","lmaccess/LOCALGROUP_INFO_1","lmaccess/LPLOCALGROUP_INFO_1","lmaccess/PLOCALGROUP_INFO_1","netmgmt.localgroup_info_1_str"]
old-location: netmgmt\localgroup_info_1_str.htm
tech.root: NetMgmt
ms.assetid: b96d7ddc-3ffb-4203-88b1-4aa123051695
ms.date: 12/05/2018
ms.keywords: '*LPLOCALGROUP_INFO_1, *PLOCALGROUP_INFO_1, LOCALGROUP_INFO_1, LOCALGROUP_INFO_1 structure [Network Management], LPLOCALGROUP_INFO_1, LPLOCALGROUP_INFO_1 structure pointer [Network Management], PLOCALGROUP_INFO_1, PLOCALGROUP_INFO_1 structure pointer [Network Management], _win32_localgroup_info_1_str, lmaccess/LOCALGROUP_INFO_1, lmaccess/LPLOCALGROUP_INFO_1, lmaccess/PLOCALGROUP_INFO_1, netmgmt.localgroup_info_1_str'
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
targetos: Windows
req.typenames: LOCALGROUP_INFO_1, *PLOCALGROUP_INFO_1, *LPLOCALGROUP_INFO_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LOCALGROUP_INFO_1
 - lmaccess/_LOCALGROUP_INFO_1
 - PLOCALGROUP_INFO_1
 - lmaccess/PLOCALGROUP_INFO_1
 - LOCALGROUP_INFO_1
 - lmaccess/LOCALGROUP_INFO_1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - LOCALGROUP_INFO_1
---

# LOCALGROUP_INFO_1 structure


## -description

The
				<b>LOCALGROUP_INFO_1</b> structure contains a local group name and a comment describing the local group.

## -struct-fields

### -field lgrpi1_name

Pointer to a Unicode string that specifies a local group name. For more information, see the following Remarks section. 




This member is ignored when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupsetinfo">NetLocalGroupSetInfo</a> function.

### -field lgrpi1_comment

Pointer to a Unicode string that contains a remark associated with the local group. This member can be a null string. The comment can have as many as MAXCOMMENTSZ characters.

## -remarks

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

## -see-also

<a href="/windows/desktop/NetMgmt/local-group-functions">Local Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupadd">NetLocalGroupAdd</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupenum">NetLocalGroupEnum</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupgetinfo">NetLocalGroupGetInfo</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupsetinfo">NetLocalGroupSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>