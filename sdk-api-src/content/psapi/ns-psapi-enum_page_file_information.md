---
UID: NS:psapi._ENUM_PAGE_FILE_INFORMATION
title: ENUM_PAGE_FILE_INFORMATION (psapi.h)
description: Contains information about a pagefile.
helpviewer_keywords: ["*PENUM_PAGE_FILE_INFORMATION","ENUM_PAGE_FILE_INFORMATION","ENUM_PAGE_FILE_INFORMATION structure [PSAPI]","PENUM_PAGE_FILE_INFORMATION","PENUM_PAGE_FILE_INFORMATION structure pointer [PSAPI]","_win32_enum_page_file_information_str","base.enum_page_file_information_str","psapi.enum_page_file_information_str","psapi/ENUM_PAGE_FILE_INFORMATION","psapi/PENUM_PAGE_FILE_INFORMATION"]
old-location: psapi\enum_page_file_information_str.htm
tech.root: psapi
ms.assetid: 020f3be8-f624-4788-8079-0f7679c9bef0
ms.date: 12/05/2018
ms.keywords: '*PENUM_PAGE_FILE_INFORMATION, ENUM_PAGE_FILE_INFORMATION, ENUM_PAGE_FILE_INFORMATION structure [PSAPI], PENUM_PAGE_FILE_INFORMATION, PENUM_PAGE_FILE_INFORMATION structure pointer [PSAPI], _win32_enum_page_file_information_str, base.enum_page_file_information_str, psapi.enum_page_file_information_str, psapi/ENUM_PAGE_FILE_INFORMATION, psapi/PENUM_PAGE_FILE_INFORMATION'
req.header: psapi.h
req.include-header: 
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
req.typenames: ENUM_PAGE_FILE_INFORMATION, *PENUM_PAGE_FILE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENUM_PAGE_FILE_INFORMATION
 - psapi/_ENUM_PAGE_FILE_INFORMATION
 - PENUM_PAGE_FILE_INFORMATION
 - psapi/PENUM_PAGE_FILE_INFORMATION
 - ENUM_PAGE_FILE_INFORMATION
 - psapi/ENUM_PAGE_FILE_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Psapi.h
api_name:
 - ENUM_PAGE_FILE_INFORMATION
---

# ENUM_PAGE_FILE_INFORMATION structure


## -description

Contains information about a pagefile.

## -struct-fields

### -field cb

The size of this structure, in bytes.

### -field Reserved

This member is reserved.

### -field TotalSize

The total size of the pagefile, in pages.

### -field TotalInUse

The current pagefile usage, in pages.

### -field PeakUsage

The peak pagefile usage, in pages.

## -see-also

<a href="/windows/desktop/api/psapi/nc-psapi-penum_page_file_callbacka">EnumPageFilesProc</a>