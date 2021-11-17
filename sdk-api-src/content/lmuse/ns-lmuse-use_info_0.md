---
UID: NS:lmuse._USE_INFO_0
title: USE_INFO_0 (lmuse.h)
description: The USE_INFO_0 structure contains the name of a shared resource and the local device redirected to it.
helpviewer_keywords: ["*LPUSE_INFO_0","*PUSE_INFO_0","LPUSE_INFO_0","LPUSE_INFO_0 structure pointer [Network Management]","PUSE_INFO_0","PUSE_INFO_0 structure pointer [Network Management]","USE_INFO_0","USE_INFO_0 structure [Network Management]","_win32_use_info_0_str","lmuse/LPUSE_INFO_0","lmuse/PUSE_INFO_0","lmuse/USE_INFO_0","netmgmt.use_info_0_str"]
old-location: netmgmt\use_info_0_str.htm
tech.root: NetMgmt
ms.assetid: 86db3f19-84c5-4e89-82cb-f01d17dcf4ec
ms.date: 12/05/2018
ms.keywords: '*LPUSE_INFO_0, *PUSE_INFO_0, LPUSE_INFO_0, LPUSE_INFO_0 structure pointer [Network Management], PUSE_INFO_0, PUSE_INFO_0 structure pointer [Network Management], USE_INFO_0, USE_INFO_0 structure [Network Management], _win32_use_info_0_str, lmuse/LPUSE_INFO_0, lmuse/PUSE_INFO_0, lmuse/USE_INFO_0, netmgmt.use_info_0_str'
req.header: lmuse.h
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
req.typenames: USE_INFO_0, *PUSE_INFO_0, *LPUSE_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USE_INFO_0
 - lmuse/_USE_INFO_0
 - PUSE_INFO_0
 - lmuse/PUSE_INFO_0
 - USE_INFO_0
 - lmuse/USE_INFO_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmuse.h
api_name:
 - USE_INFO_0
---

# USE_INFO_0 structure


## -description

The
				<b>USE_INFO_0</b> structure contains the name of a shared resource and the local device redirected to it.

## -struct-fields

### -field ui0_local

Pointer to a Unicode string that specifies the local device name (for example, drive E or LPT1) being redirected to the shared resource. The constant DEVLEN specifies the maximum number of characters in the string.

### -field ui0_remote

Pointer to a Unicode string that specifies the share name of the remote resource being accessed. The string is in the form: 





``` syntax
\\servername\sharename

```


## -see-also

<a href="/windows/desktop/api/lmuse/nf-lmuse-netuseenum">NetUseEnum</a>



<a href="/windows/desktop/api/lmuse/nf-lmuse-netusegetinfo">NetUseGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/use-functions">Use Functions</a>
