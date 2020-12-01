---
UID: NS:lmshare._SHARE_INFO_1004
title: SHARE_INFO_1004 (lmshare.h)
description: Contains a comment associated with the shared resource.
helpviewer_keywords: ["*LPSHARE_INFO_1004","*PSHARE_INFO_1004","LPSHARE_INFO_1004","LPSHARE_INFO_1004 structure pointer [Files]","PSHARE_INFO_1004","PSHARE_INFO_1004 structure pointer [Files]","SHARE_INFO_1004","SHARE_INFO_1004 structure [Files]","_win32_share_info_1004_str","fs.share_info_1004_str","lmshare/LPSHARE_INFO_1004","lmshare/PSHARE_INFO_1004","lmshare/SHARE_INFO_1004","netmgmt.share_info_1004_str"]
old-location: fs\share_info_1004_str.htm
tech.root: fs
ms.assetid: 41749066-d0e2-4a6b-aea5-216af9a530f4
ms.date: 12/05/2018
ms.keywords: '*LPSHARE_INFO_1004, *PSHARE_INFO_1004, LPSHARE_INFO_1004, LPSHARE_INFO_1004 structure pointer [Files], PSHARE_INFO_1004, PSHARE_INFO_1004 structure pointer [Files], SHARE_INFO_1004, SHARE_INFO_1004 structure [Files], _win32_share_info_1004_str, fs.share_info_1004_str, lmshare/LPSHARE_INFO_1004, lmshare/PSHARE_INFO_1004, lmshare/SHARE_INFO_1004, netmgmt.share_info_1004_str'
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
req.typenames: SHARE_INFO_1004, *PSHARE_INFO_1004, *LPSHARE_INFO_1004
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHARE_INFO_1004
 - lmshare/_SHARE_INFO_1004
 - PSHARE_INFO_1004
 - lmshare/PSHARE_INFO_1004
 - SHARE_INFO_1004
 - lmshare/SHARE_INFO_1004
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
 - SHARE_INFO_1004
---

# SHARE_INFO_1004 structure


## -description

Contains a comment associated with the shared resource.

## -struct-fields

### -field shi1004_remark

Pointer to a Unicode string that contains an optional comment about the shared resource.

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>