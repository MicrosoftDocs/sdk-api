---
UID: NS:immdev.tagRECONVERTSTRING
title: RECONVERTSTRING (immdev.h)
description: The RECONVERTSTRING structure (immdev.h) defines the strings for IME reconversion. 
helpviewer_keywords: ["*LPRECONVERTSTRING","*NPRECONVERTSTRING","*PRECONVERTSTRING","PRECONVERTSTRING","PRECONVERTSTRING structure pointer [Internationalization for Windows Applications]","RECONVERTSTRING","RECONVERTSTRING structure [Internationalization for Windows Applications]","_win32_RECONVERTSTRING_str","imm/PRECONVERTSTRING","imm/RECONVERTSTRING","intl.reconvertstring","tagRECONVERTSTRING"]
old-location: intl\reconvertstring.htm
tech.root: Intl
ms.assetid: 66c97e0d-d196-4062-8094-f31012b9bbb7
ms.date: 08/05/2022
ms.keywords: '*LPRECONVERTSTRING, *NPRECONVERTSTRING, *PRECONVERTSTRING, PRECONVERTSTRING, PRECONVERTSTRING structure pointer [Internationalization for Windows Applications], RECONVERTSTRING, RECONVERTSTRING structure [Internationalization for Windows Applications], _win32_RECONVERTSTRING_str, imm/PRECONVERTSTRING, imm/RECONVERTSTRING, intl.reconvertstring, tagRECONVERTSTRING'
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: RECONVERTSTRING, *PRECONVERTSTRING, *NPRECONVERTSTRING, *LPRECONVERTSTRING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRECONVERTSTRING
 - immdev/tagRECONVERTSTRING
 - PRECONVERTSTRING
 - immdev/PRECONVERTSTRING
 - RECONVERTSTRING
 - immdev/RECONVERTSTRING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Imm.h
api_name:
 - RECONVERTSTRING
---

# RECONVERTSTRING structure


## -description

Defines the strings for IME reconversion. It is the first item in a memory block that contains the strings for reconversion.

## -struct-fields

### -field dwSize

Size of this structure and the memory block it heads.

### -field dwVersion

Version number. Must be 0.

### -field dwStrLen

Length of the string that contains the composition string.

### -field dwStrOffset

Offset from the start position of this structure.

### -field dwCompStrLen

Length of the string that will be the composition string.

### -field dwCompStrOffset

Offset of the string that will be the composition string.

### -field dwTargetStrLen

Length of the string that is related to the target clause in the composition string.

### -field dwTargetStrOffset

Offset of the target string.

## -remarks

The <b>dwCompStrOffset</b> and <b>dwTargetOffset</b> members are the relative positions in <b>dwStrOffset</b>. For a Unicode IME, <b>dwStrLen</b>, <b>dwCompStrLen</b>, and <b>dwTargetStrLen</b> are TCHAR values, that is, character counts. The members <b>dwStrOffset</b>, <b>dwCompStrOffset</b>, and <b>dwTargetStrOffset</b> specify byte counts.

If an application starts the reconversion process by calling <a href="/windows/desktop/api/imm/nf-imm-immsetcompositionstringa">ImmSetCompositionString</a> with SCS_SETRECONVERTSTRING and SCS_QUERYRECONVERTSTRING, the application must allocate the necessary memory for the <b>RECONVERTSTRING</b> structure as well as the composition string buffer. IME should not use this memory later. If IME starts the process, IME should allocate necessary memory for the structure and the composition string buffer.

## -see-also

<a href="/windows/desktop/Intl/imr-confirmreconvertstring">IMR_CONFIRMRECONVERTSTRING</a>



<a href="/windows/desktop/Intl/imr-reconvertstring">IMR_RECONVERTSTRING</a>



<a href="/windows/desktop/api/imm/nf-imm-immsetcompositionstringa">ImmSetCompositionString</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-structures">Input Method Manager Structures</a>
