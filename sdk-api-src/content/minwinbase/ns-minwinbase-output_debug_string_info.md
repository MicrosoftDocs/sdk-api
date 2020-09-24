---
UID: NS:minwinbase._OUTPUT_DEBUG_STRING_INFO
title: OUTPUT_DEBUG_STRING_INFO (minwinbase.h)
description: Contains the address, format, and length, in bytes, of a debugging string.
helpviewer_keywords: ["*LPOUTPUT_DEBUG_STRING_INFO","LPOUTPUT_DEBUG_STRING_INFO","LPOUTPUT_DEBUG_STRING_INFO structure pointer","OUTPUT_DEBUG_STRING_INFO","OUTPUT_DEBUG_STRING_INFO structure","_OUTPUT_DEBUG_STRING_INFO","_win32_output_debug_string_info_str","base.output_debug_string_info_str","minwinbase/LPOUTPUT_DEBUG_STRING_INFO","minwinbase/OUTPUT_DEBUG_STRING_INFO"]
old-location: base\output_debug_string_info_str.htm
tech.root: Debug
ms.assetid: 43594bf5-ee79-4334-b0d4-92b2b41bf35a
ms.date: 12/05/2018
ms.keywords: '*LPOUTPUT_DEBUG_STRING_INFO, LPOUTPUT_DEBUG_STRING_INFO, LPOUTPUT_DEBUG_STRING_INFO structure pointer, OUTPUT_DEBUG_STRING_INFO, OUTPUT_DEBUG_STRING_INFO structure, _OUTPUT_DEBUG_STRING_INFO, _win32_output_debug_string_info_str, base.output_debug_string_info_str, minwinbase/LPOUTPUT_DEBUG_STRING_INFO, minwinbase/OUTPUT_DEBUG_STRING_INFO'
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
targetos: Windows
req.typenames: OUTPUT_DEBUG_STRING_INFO, *LPOUTPUT_DEBUG_STRING_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OUTPUT_DEBUG_STRING_INFO
 - minwinbase/_OUTPUT_DEBUG_STRING_INFO
 - LPOUTPUT_DEBUG_STRING_INFO
 - minwinbase/LPOUTPUT_DEBUG_STRING_INFO
 - OUTPUT_DEBUG_STRING_INFO
 - minwinbase/OUTPUT_DEBUG_STRING_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minwinbase.h
api_name:
 - OUTPUT_DEBUG_STRING_INFO
---

# OUTPUT_DEBUG_STRING_INFO structure


## -description

Contains the address, format, and length, in bytes, of a debugging string.

## -struct-fields

### -field lpDebugStringData

The debugging string in the calling process's address space. The debugger can use the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a> function to retrieve the value of the string.

### -field fUnicode

The format of the debugging string. If this member is zero, the debugging string is ANSI; if it is nonzero, the string is Unicode.

### -field nDebugStringLength

The lower 16 bits of the length of the string in bytes. As nDebugStringLength is of type WORD, this does not always contain the full length of the string in bytes.

For example, if the original output string is longer than 65536 bytes, this field will contain a value that is less than the actual string length in bytes.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-debug_event">DEBUG_EVENT</a>

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a>