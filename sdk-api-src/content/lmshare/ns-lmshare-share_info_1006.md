---
UID: NS:lmshare._SHARE_INFO_1006
title: SHARE_INFO_1006 (lmshare.h)
description: Specifies the maximum number of concurrent connections that the shared resource can accommodate.
helpviewer_keywords: ["*LPSHARE_INFO_1006","*PSHARE_INFO_1006","LPSHARE_INFO_1006","LPSHARE_INFO_1006 structure pointer [Files]","PSHARE_INFO_1006","PSHARE_INFO_1006 structure pointer [Files]","SHARE_INFO_1006","SHARE_INFO_1006 structure [Files]","_win32_share_info_1006_str","fs.share_info_1006_str","lmshare/LPSHARE_INFO_1006","lmshare/PSHARE_INFO_1006","lmshare/SHARE_INFO_1006","netmgmt.share_info_1006_str"]
old-location: fs\share_info_1006_str.htm
tech.root: fs
ms.assetid: 645a8670-5661-4d6c-8d9e-67c1bbb0f1d7
ms.date: 12/05/2018
ms.keywords: '*LPSHARE_INFO_1006, *PSHARE_INFO_1006, LPSHARE_INFO_1006, LPSHARE_INFO_1006 structure pointer [Files], PSHARE_INFO_1006, PSHARE_INFO_1006 structure pointer [Files], SHARE_INFO_1006, SHARE_INFO_1006 structure [Files], _win32_share_info_1006_str, fs.share_info_1006_str, lmshare/LPSHARE_INFO_1006, lmshare/PSHARE_INFO_1006, lmshare/SHARE_INFO_1006, netmgmt.share_info_1006_str'
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
req.typenames: SHARE_INFO_1006, *PSHARE_INFO_1006, *LPSHARE_INFO_1006
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHARE_INFO_1006
 - lmshare/_SHARE_INFO_1006
 - PSHARE_INFO_1006
 - lmshare/PSHARE_INFO_1006
 - SHARE_INFO_1006
 - lmshare/SHARE_INFO_1006
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
 - SHARE_INFO_1006
---

# SHARE_INFO_1006 structure


## -description

Specifies the maximum number of concurrent connections that the shared resource can accommodate.

## -struct-fields

### -field shi1006_max_uses

Specifies a DWORD value that indicates the maximum number of concurrent connections that the shared resource can accommodate. The number of connections is unlimited if the value specified in this member is –1.

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>