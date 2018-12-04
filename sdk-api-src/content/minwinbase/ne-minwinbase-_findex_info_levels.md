---
UID: NE:minwinbase._FINDEX_INFO_LEVELS
title: "_FINDEX_INFO_LEVELS"
author: windows-sdk-content
description: Defines values that are used with the FindFirstFileEx function to specify the information level of the returned data.
old-location: fs\findex_info_levels_str.htm
tech.root: fileio
ms.assetid: 454d5fc2-2ada-49de-9e1e-9e6eba050b17
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: FINDEX_INFO_LEVELS, FINDEX_INFO_LEVELS enumeration [Files], FindExInfoBasic, FindExInfoMaxInfoLevel, FindExInfoStandard, _FINDEX_INFO_LEVELS, _win32_findex_info_levels_str, base.findex_info_levels_str, fs.findex_info_levels_str, winbase/FINDEX_INFO_LEVELS, winbase/FindExInfoBasic, winbase/FindExInfoMaxInfoLevel, winbase/FindExInfoStandard
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - FINDEX_INFO_LEVELS
product: Windows
targetos: Windows
req.typenames: FINDEX_INFO_LEVELS
req.redist: 
---

# _FINDEX_INFO_LEVELS enumeration


## -description


Defines values that are used with the 
    <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a> function to specify the information 
    level of the returned data.


## -enum-fields




### -field FindExInfoStandard

The <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a> function retrieves a 
      standard set of attribute information. The data is returned in a 
      <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure.


### -field FindExInfoBasic

The <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a> function does not query the short file name, improving overall enumeration speed. The data is returned in a 
      <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure, and the <b>cAlternateFileName</b> 
    member is always a <b>NULL</b> string.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7.


### -field FindExInfoMaxInfoLevel

This value is used for validation. Supported values are less than this value.


## -see-also




<a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a>



<a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a>
 

 

