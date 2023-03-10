---
UID: NE:minwinbase._FINDEX_INFO_LEVELS
title: FINDEX_INFO_LEVELS (minwinbase.h)
description: Defines values that are used with the FindFirstFileEx function to specify the information level of the returned data.
helpviewer_keywords: ["FINDEX_INFO_LEVELS","FINDEX_INFO_LEVELS enumeration [Files]","FindExInfoBasic","FindExInfoMaxInfoLevel","FindExInfoStandard","_win32_findex_info_levels_str","base.findex_info_levels_str","fs.findex_info_levels_str","winbase/FINDEX_INFO_LEVELS","winbase/FindExInfoBasic","winbase/FindExInfoMaxInfoLevel","winbase/FindExInfoStandard"]
old-location: fs\findex_info_levels_str.htm
tech.root: fs
ms.assetid: 454d5fc2-2ada-49de-9e1e-9e6eba050b17
ms.date: 12/05/2018
ms.keywords: FINDEX_INFO_LEVELS, FINDEX_INFO_LEVELS enumeration [Files], FindExInfoBasic, FindExInfoMaxInfoLevel, FindExInfoStandard, _win32_findex_info_levels_str, base.findex_info_levels_str, fs.findex_info_levels_str, winbase/FINDEX_INFO_LEVELS, winbase/FindExInfoBasic, winbase/FindExInfoMaxInfoLevel, winbase/FindExInfoStandard
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
req.typenames: FINDEX_INFO_LEVELS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FINDEX_INFO_LEVELS
 - minwinbase/_FINDEX_INFO_LEVELS
 - FINDEX_INFO_LEVELS
 - minwinbase/FINDEX_INFO_LEVELS
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
 - FINDEX_INFO_LEVELS
---

# FINDEX_INFO_LEVELS enumeration


## -description

Defines values that are used with the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexa">FindFirstFileEx</a> function to specify the information 
    level of the returned data.

## -enum-fields

### -field FindExInfoStandard

The <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexa">FindFirstFileEx</a> function retrieves a 
      standard set of attribute information. The data is returned in a 
      <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure.

### -field FindExInfoBasic

The <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexa">FindFirstFileEx</a> function does not query the short file name, improving overall enumeration speed. The data is returned in a 
      <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure, and the <b>cAlternateFileName</b> 
    member is always a <b>NULL</b> string.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7.

### -field FindExInfoMaxInfoLevel

This value is used for validation. Supported values are less than this value.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexa">FindFirstFileEx</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a>