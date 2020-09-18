---
UID: NE:fileapi._STREAM_INFO_LEVELS
title: STREAM_INFO_LEVELS (fileapi.h)
description: Defines values that are used with the FindFirstStreamW function to specify the information level of the returned data.
helpviewer_keywords: ["FindStreamInfoMaxInfoLevel","FindStreamInfoStandard","STREAM_INFO_LEVELS","STREAM_INFO_LEVELS enumeration [Files]","_win32_stream_info_levels","base.stream_info_levels","fileapi/FindStreamInfoMaxInfoLevel","fileapi/FindStreamInfoStandard","fileapi/STREAM_INFO_LEVELS","fs.stream_info_levels"]
old-location: fs\stream_info_levels.htm
tech.root: fs
ms.assetid: 411efcdc-e13a-4f27-a3da-31dff714e415
ms.date: 12/05/2018
ms.keywords: FindStreamInfoMaxInfoLevel, FindStreamInfoStandard, STREAM_INFO_LEVELS, STREAM_INFO_LEVELS enumeration [Files], _win32_stream_info_levels, base.stream_info_levels, fileapi/FindStreamInfoMaxInfoLevel, fileapi/FindStreamInfoStandard, fileapi/STREAM_INFO_LEVELS, fs.stream_info_levels
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: STREAM_INFO_LEVELS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _STREAM_INFO_LEVELS
 - fileapi/_STREAM_INFO_LEVELS
 - STREAM_INFO_LEVELS
 - fileapi/STREAM_INFO_LEVELS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fileapi.h
api_name:
 - STREAM_INFO_LEVELS
---

# STREAM_INFO_LEVELS enumeration


## -description

Defines values that are used with the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw">FindFirstStreamW</a> function to specify the information 
    level of the returned data.

## -enum-fields

### -field FindStreamInfoStandard

The <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw">FindFirstStreamW</a> function retrieves standard 
      stream information. The data is returned in a 
      <a href="/windows/desktop/api/fileapi/ns-fileapi-win32_find_stream_data">WIN32_FIND_STREAM_DATA</a> structure.

### -field FindStreamInfoMaxInfoLevel

Used to determine valid enumeration values. All supported enumeration values are less than 
      <b>FindStreamInfoMaxInfoLevel</b>.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw">FindFirstStreamW</a>



<a href="/windows/desktop/api/fileapi/ns-fileapi-win32_find_stream_data">WIN32_FIND_STREAM_DATA</a>