---
UID: NS:minwinbase._OUTPUT_DEBUG_STRING_INFO
title: "_OUTPUT_DEBUG_STRING_INFO"
author: windows-sdk-content
description: Contains the address, format, and length, in bytes, of a debugging string.
old-location: base\output_debug_string_info_str.htm
tech.root: debug
ms.assetid: 43594bf5-ee79-4334-b0d4-92b2b41bf35a
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPOUTPUT_DEBUG_STRING_INFO, LPOUTPUT_DEBUG_STRING_INFO, LPOUTPUT_DEBUG_STRING_INFO structure pointer, OUTPUT_DEBUG_STRING_INFO, OUTPUT_DEBUG_STRING_INFO structure, _OUTPUT_DEBUG_STRING_INFO, _win32_output_debug_string_info_str, base.output_debug_string_info_str, minwinbase/LPOUTPUT_DEBUG_STRING_INFO, minwinbase/OUTPUT_DEBUG_STRING_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: minwinbase.h
req.include-header: Windows.h
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
 - minwinbase.h
api_name:
 - OUTPUT_DEBUG_STRING_INFO
product: Windows
targetos: Windows
req.typenames: OUTPUT_DEBUG_STRING_INFO, *LPOUTPUT_DEBUG_STRING_INFO
req.redist: 
---

# _OUTPUT_DEBUG_STRING_INFO structure


## -description


Contains the address, format, and length, in bytes, of a debugging string.


## -struct-fields




### -field lpDebugStringData

The debugging string in the calling process's address space. The debugger can use the 
<a href="https://msdn.microsoft.com/8774e145-ee7f-44de-85db-0445b905f986">ReadProcessMemory</a> function to retrieve the value of the string.


### -field fUnicode

The format of the debugging string. If this member is zero, the debugging string is ANSI; if it is nonzero, the string is Unicode.


### -field nDebugStringLength

The size of the debugging string, in characters. The length includes the string's terminating null character.


## -see-also




<a href="https://msdn.microsoft.com/056aa7ee-51ca-48ec-9cd7-26085bb85b11">DEBUG_EVENT</a>



<a href="https://msdn.microsoft.com/8774e145-ee7f-44de-85db-0445b905f986">ReadProcessMemory</a>
 

 

