---
UID: NS:lmshare._FILE_INFO_2
title: FILE_INFO_2 (lmshare.h)
description: Contains the identification number for a file, device, or pipe.
helpviewer_keywords: ["*LPFILE_INFO_2","*PFILE_INFO_2","FILE_INFO_2","FILE_INFO_2 structure [Files]","LPFILE_INFO_2","LPFILE_INFO_2 structure pointer [Files]","PFILE_INFO_2","PFILE_INFO_2 structure pointer [Files]","_win32_file_info_2_str","fs.file_info_2_str","lmshare/FILE_INFO_2","lmshare/LPFILE_INFO_2","lmshare/PFILE_INFO_2","netmgmt.file_info_2_str"]
old-location: fs\file_info_2_str.htm
tech.root: fs
ms.assetid: c80090d5-7064-4809-9185-02116f7ac2ef
ms.date: 12/05/2018
ms.keywords: '*LPFILE_INFO_2, *PFILE_INFO_2, FILE_INFO_2, FILE_INFO_2 structure [Files], LPFILE_INFO_2, LPFILE_INFO_2 structure pointer [Files], PFILE_INFO_2, PFILE_INFO_2 structure pointer [Files], _win32_file_info_2_str, fs.file_info_2_str, lmshare/FILE_INFO_2, lmshare/LPFILE_INFO_2, lmshare/PFILE_INFO_2, netmgmt.file_info_2_str'
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
req.typenames: FILE_INFO_2, *PFILE_INFO_2, *LPFILE_INFO_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILE_INFO_2
 - lmshare/_FILE_INFO_2
 - PFILE_INFO_2
 - lmshare/PFILE_INFO_2
 - FILE_INFO_2
 - lmshare/FILE_INFO_2
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
 - FILE_INFO_2
---

# FILE_INFO_2 structure


## -description

Contains the identification number for a file, device, or pipe.

## -struct-fields

### -field fi2_id

Specifies a DWORD value that contains the identification number assigned to the resource when it is opened.

## -see-also

<a href="/windows/desktop/api/lmshare/ns-lmshare-file_info_3">FILE_INFO_3</a>



<a href="/windows/desktop/NetShare/netfile-functions">NetFile Functions</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netfileenum">NetFileEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo">NetFileGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>