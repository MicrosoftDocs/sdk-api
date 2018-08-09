---
UID: NS:imm.tagRECONVERTSTRING
title: tagRECONVERTSTRING
author: windows-sdk-content
description: Defines the strings for IME reconversion. It is the first item in a memory block that contains the strings for reconversion.
old-location: intl\reconvertstring.htm
old-project: Intl
ms.assetid: 66c97e0d-d196-4062-8094-f31012b9bbb7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPRECONVERTSTRING, *NPRECONVERTSTRING, *PRECONVERTSTRING, PRECONVERTSTRING, PRECONVERTSTRING structure pointer [Internationalization for Windows Applications], RECONVERTSTRING, RECONVERTSTRING structure [Internationalization for Windows Applications], _win32_RECONVERTSTRING_str, imm/PRECONVERTSTRING, imm/RECONVERTSTRING, intl.reconvertstring, tagRECONVERTSTRING"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: imm.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: RECONVERTSTRING, *PRECONVERTSTRING, *NPRECONVERTSTRING, *LPRECONVERTSTRING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Imm.h
api_name:
 - RECONVERTSTRING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagRECONVERTSTRING structure


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

If an application starts the reconversion process by calling <a href="https://msdn.microsoft.com/0bac534d-d2a8-4dbc-8062-f1d2a8ca0c34">ImmSetCompositionString</a> with SCS_SETRECONVERTSTRING and SCS_QUERYRECONVERTSTRING, the application must allocate the necessary memory for the <b>RECONVERTSTRING</b> structure as well as the composition string buffer. IME should not use this memory later. If IME starts the process, IME should allocate necessary memory for the structure and the composition string buffer.




## -see-also




<a href="https://msdn.microsoft.com/035a7072-d292-4883-bc3e-d1e9ed64d9ec">IMR_CONFIRMRECONVERTSTRING</a>



<a href="https://msdn.microsoft.com/82ef20b5-bdfa-4bde-abb4-3d14ae35c116">IMR_RECONVERTSTRING</a>



<a href="https://msdn.microsoft.com/0bac534d-d2a8-4dbc-8062-f1d2a8ca0c34">ImmSetCompositionString</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/1be3ae8b-e083-4420-bc8a-7f49c4264cab">Input Method Manager Structures</a>
 

 

