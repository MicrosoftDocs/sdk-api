---
UID: NS:lmshare._SHARE_INFO_0
title: SHARE_INFO_0 (lmshare.h)
description: Contains the name of the shared resource.
helpviewer_keywords: ["*LPSHARE_INFO_0","*PSHARE_INFO_0","LPSHARE_INFO_0","LPSHARE_INFO_0 structure pointer [Files]","PSHARE_INFO_0","PSHARE_INFO_0 structure pointer [Files]","SHARE_INFO_0","SHARE_INFO_0 structure [Files]","_win32_share_info_0_str","fs.share_info_0_str","lmshare/LPSHARE_INFO_0","lmshare/PSHARE_INFO_0","lmshare/SHARE_INFO_0","netmgmt.share_info_0_str"]
old-location: fs\share_info_0_str.htm
tech.root: fs
ms.assetid: 47a74c71-1fcb-4c49-93b5-ea7cf3a0e567
ms.date: 12/05/2018
ms.keywords: '*LPSHARE_INFO_0, *PSHARE_INFO_0, LPSHARE_INFO_0, LPSHARE_INFO_0 structure pointer [Files], PSHARE_INFO_0, PSHARE_INFO_0 structure pointer [Files], SHARE_INFO_0, SHARE_INFO_0 structure [Files], _win32_share_info_0_str, fs.share_info_0_str, lmshare/LPSHARE_INFO_0, lmshare/PSHARE_INFO_0, lmshare/SHARE_INFO_0, netmgmt.share_info_0_str'
req.header: lmshare.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SHARE_INFO_0, *PSHARE_INFO_0, *LPSHARE_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHARE_INFO_0
 - lmshare/_SHARE_INFO_0
 - PSHARE_INFO_0
 - lmshare/PSHARE_INFO_0
 - SHARE_INFO_0
 - lmshare/SHARE_INFO_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmshare.h
api_name:
 - SHARE_INFO_0
---

# SHARE_INFO_0 structure


## -description

Contains the name of the shared resource.

## -struct-fields

### -field shi0_netname

Pointer to a Unicode string specifying the share name of a resource.

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netshareenum">NetShareEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>