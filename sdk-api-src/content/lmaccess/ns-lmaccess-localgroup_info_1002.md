---
UID: NS:lmaccess._LOCALGROUP_INFO_1002
title: LOCALGROUP_INFO_1002 (lmaccess.h)
description: The LOCALGROUP_INFO_1002 structure contains a comment describing a local group.
helpviewer_keywords: ["*LPLOCALGROUP_INFO_1002","*PLOCALGROUP_INFO_1002","LOCALGROUP_INFO_1002","LOCALGROUP_INFO_1002 structure [Network Management]","LPLOCALGROUP_INFO_1002","LPLOCALGROUP_INFO_1002 structure pointer [Network Management]","PLOCALGROUP_INFO_1002","PLOCALGROUP_INFO_1002 structure pointer [Network Management]","_win32_localgroup_info_1002_str","lmaccess/LOCALGROUP_INFO_1002","lmaccess/LPLOCALGROUP_INFO_1002","lmaccess/PLOCALGROUP_INFO_1002","netmgmt.localgroup_info_1002_str"]
old-location: netmgmt\localgroup_info_1002_str.htm
tech.root: NetMgmt
ms.assetid: 027db4a3-6722-46e8-a204-922ed97cb3f5
ms.date: 12/05/2018
ms.keywords: '*LPLOCALGROUP_INFO_1002, *PLOCALGROUP_INFO_1002, LOCALGROUP_INFO_1002, LOCALGROUP_INFO_1002 structure [Network Management], LPLOCALGROUP_INFO_1002, LPLOCALGROUP_INFO_1002 structure pointer [Network Management], PLOCALGROUP_INFO_1002, PLOCALGROUP_INFO_1002 structure pointer [Network Management], _win32_localgroup_info_1002_str, lmaccess/LOCALGROUP_INFO_1002, lmaccess/LPLOCALGROUP_INFO_1002, lmaccess/PLOCALGROUP_INFO_1002, netmgmt.localgroup_info_1002_str'
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
req.typenames: LOCALGROUP_INFO_1002, *PLOCALGROUP_INFO_1002, *LPLOCALGROUP_INFO_1002
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LOCALGROUP_INFO_1002
 - lmaccess/_LOCALGROUP_INFO_1002
 - PLOCALGROUP_INFO_1002
 - lmaccess/PLOCALGROUP_INFO_1002
 - LOCALGROUP_INFO_1002
 - lmaccess/LOCALGROUP_INFO_1002
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
 - LOCALGROUP_INFO_1002
---

# LOCALGROUP_INFO_1002 structure


## -description

The 
				<b>LOCALGROUP_INFO_1002</b> structure contains a comment describing a local group.

## -struct-fields

### -field lgrpi1002_comment

Pointer to a Unicode string that specifies a remark associated with the local group. This member can be a null string. The comment can have as many as MAXCOMMENTSZ characters.

## -see-also

<a href="/windows/desktop/NetMgmt/local-group-functions">Local Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupsetinfo">NetLocalGroupSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>