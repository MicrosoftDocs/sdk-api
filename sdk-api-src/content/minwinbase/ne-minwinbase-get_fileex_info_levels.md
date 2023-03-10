---
UID: NE:minwinbase._GET_FILEEX_INFO_LEVELS
title: GET_FILEEX_INFO_LEVELS (minwinbase.h)
description: Defines values that are used with the GetFileAttributesEx and GetFileAttributesTransacted functions to specify the information level of the returned data.
helpviewer_keywords: ["GET_FILEEX_INFO_LEVELS","GET_FILEEX_INFO_LEVELS enumeration [Files]","GetFileExInfoStandard","GetFileExMaxInfoLevel","fs.get_fileex_info_levels","winbase/GET_FILEEX_INFO_LEVELS","winbase/GetFileExInfoStandard","winbase/GetFileExMaxInfoLevel"]
old-location: fs\get_fileex_info_levels.htm
tech.root: fs
ms.assetid: 1004ab99-9c08-4ed4-ba5f-d72f1b44a415
ms.date: 12/05/2018
ms.keywords: GET_FILEEX_INFO_LEVELS, GET_FILEEX_INFO_LEVELS enumeration [Files], GetFileExInfoStandard, GetFileExMaxInfoLevel, fs.get_fileex_info_levels, winbase/GET_FILEEX_INFO_LEVELS, winbase/GetFileExInfoStandard, winbase/GetFileExMaxInfoLevel
req.header: minwinbase.h
req.include-header: Minwinbase.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
req.typenames: GET_FILEEX_INFO_LEVELS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GET_FILEEX_INFO_LEVELS
 - minwinbase/_GET_FILEEX_INFO_LEVELS
 - GET_FILEEX_INFO_LEVELS
 - minwinbase/GET_FILEEX_INFO_LEVELS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - GET_FILEEX_INFO_LEVELS
---

# GET_FILEEX_INFO_LEVELS enumeration


## -description

Defines values that are used with the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesexa">GetFileAttributesEx</a> and 
    <a href="/windows/desktop/api/winbase/nf-winbase-getfileattributestransacteda">GetFileAttributesTransacted</a> functions to 
    specify the information level of the returned data.

## -enum-fields

### -field GetFileExInfoStandard

The <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesexa">GetFileAttributesEx</a> or 
      <a href="/windows/desktop/api/winbase/nf-winbase-getfileattributestransacteda">GetFileAttributesTransacted</a> function 
      retrieves a standard set of attribute information. The data is returned in a 
      <a href="/windows/desktop/api/fileapi/ns-fileapi-win32_file_attribute_data">WIN32_FILE_ATTRIBUTE_DATA</a> 
      structure.

### -field GetFileExMaxInfoLevel

One greater than the maximum value. Valid values for this enumeration will be less than this value.

## -see-also

<a href="/windows/desktop/FileIO/file-management-enumerations">File Management Enumerations</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesexa">GetFileAttributesEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileattributestransacteda">GetFileAttributesTransacted</a>



<a href="/windows/desktop/api/fileapi/ns-fileapi-win32_file_attribute_data">WIN32_FILE_ATTRIBUTE_DATA</a>