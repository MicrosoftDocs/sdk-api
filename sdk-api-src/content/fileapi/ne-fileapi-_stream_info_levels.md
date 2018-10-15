---
UID: NE:fileapi._STREAM_INFO_LEVELS
title: "_STREAM_INFO_LEVELS"
author: windows-sdk-content
description: Defines values that are used with the FindFirstStreamW function to specify the information level of the returned data.
old-location: fs\stream_info_levels.htm
tech.root: FileIO
ms.assetid: 411efcdc-e13a-4f27-a3da-31dff714e415
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: FindStreamInfoMaxInfoLevel, FindStreamInfoStandard, STREAM_INFO_LEVELS, STREAM_INFO_LEVELS enumeration [Files], _STREAM_INFO_LEVELS, _win32_stream_info_levels, base.stream_info_levels, fileapi/FindStreamInfoMaxInfoLevel, fileapi/FindStreamInfoStandard, fileapi/STREAM_INFO_LEVELS, fs.stream_info_levels
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fileapi.h
api_name:
 - STREAM_INFO_LEVELS
product: Windows
targetos: Windows
req.typenames: STREAM_INFO_LEVELS
req.redist: 
---

# _STREAM_INFO_LEVELS enumeration


## -description


Defines values that are used with the 
    <a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a> function to specify the information 
    level of the returned data.


## -enum-fields




### -field FindStreamInfoStandard

The <a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a> function retrieves standard 
      stream information. The data is returned in a 
      <a href="https://msdn.microsoft.com/f21f5161-10a8-474c-85d8-dde075b9daff">WIN32_FIND_STREAM_DATA</a> structure.


### -field FindStreamInfoMaxInfoLevel

Used to determine valid enumeration values. All supported enumeration values are less than 
      <b>FindStreamInfoMaxInfoLevel</b>.


## -see-also




<a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a>



<a href="https://msdn.microsoft.com/f21f5161-10a8-474c-85d8-dde075b9daff">WIN32_FIND_STREAM_DATA</a>
 

 

