---
UID: NS:psapi._ENUM_PAGE_FILE_INFORMATION
title: ENUM_PAGE_FILE_INFORMATION
author: windows-sdk-content
description: Contains information about a pagefile.
old-location: psapi\enum_page_file_information_str.htm
tech.root: psapi
ms.assetid: 020f3be8-f624-4788-8079-0f7679c9bef0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PENUM_PAGE_FILE_INFORMATION, ENUM_PAGE_FILE_INFORMATION, ENUM_PAGE_FILE_INFORMATION structure [PSAPI], PENUM_PAGE_FILE_INFORMATION, PENUM_PAGE_FILE_INFORMATION structure pointer [PSAPI], _win32_enum_page_file_information_str, base.enum_page_file_information_str, psapi.enum_page_file_information_str, psapi/ENUM_PAGE_FILE_INFORMATION, psapi/PENUM_PAGE_FILE_INFORMATION"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Psapi.h
api_name:
 - ENUM_PAGE_FILE_INFORMATION
product: Windows
targetos: Windows
req.typenames: ENUM_PAGE_FILE_INFORMATION, *PENUM_PAGE_FILE_INFORMATION
req.redist: 
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




<a href="https://msdn.microsoft.com/eb3610fb-2c95-4f7b-973d-8dc41d2829f1">EnumPageFilesProc</a>
 

 

