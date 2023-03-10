---
UID: NS:lmshare._SHARE_INFO_1501
title: SHARE_INFO_1501 (lmshare.h)
description: Contains the security descriptor associated with the specified share. For more information, see Security Descriptors.
helpviewer_keywords: ["*LPSHARE_INFO_1501","*PSHARE_INFO_1501","LPSHARE_INFO_1501","LPSHARE_INFO_1501 structure pointer [Files]","PSHARE_INFO_1501","PSHARE_INFO_1501 structure pointer [Files]","SHARE_INFO_1501","SHARE_INFO_1501 structure [Files]","_win32_share_info_1501_str","fs.share_info_1501_str","lmshare/LPSHARE_INFO_1501","lmshare/PSHARE_INFO_1501","lmshare/SHARE_INFO_1501","netmgmt.share_info_1501_str"]
old-location: fs\share_info_1501_str.htm
tech.root: fs
ms.assetid: ef5d4936-8c0b-4a3c-b2b9-34868eb01a2e
ms.date: 12/05/2018
ms.keywords: '*LPSHARE_INFO_1501, *PSHARE_INFO_1501, LPSHARE_INFO_1501, LPSHARE_INFO_1501 structure pointer [Files], PSHARE_INFO_1501, PSHARE_INFO_1501 structure pointer [Files], SHARE_INFO_1501, SHARE_INFO_1501 structure [Files], _win32_share_info_1501_str, fs.share_info_1501_str, lmshare/LPSHARE_INFO_1501, lmshare/PSHARE_INFO_1501, lmshare/SHARE_INFO_1501, netmgmt.share_info_1501_str'
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
req.typenames: SHARE_INFO_1501, *PSHARE_INFO_1501, *LPSHARE_INFO_1501
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHARE_INFO_1501
 - lmshare/_SHARE_INFO_1501
 - PSHARE_INFO_1501
 - lmshare/PSHARE_INFO_1501
 - SHARE_INFO_1501
 - lmshare/SHARE_INFO_1501
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
 - SHARE_INFO_1501
---

# SHARE_INFO_1501 structure


## -description

Contains the security descriptor associated with the specified share. For more information, see <a href="/windows/desktop/SecAuthZ/security-descriptors">Security Descriptors</a>.

## -struct-fields

### -field shi1501_reserved

Reserved; must be zero.

### -field shi1501_security_descriptor

Specifies the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> associated with the share.

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>