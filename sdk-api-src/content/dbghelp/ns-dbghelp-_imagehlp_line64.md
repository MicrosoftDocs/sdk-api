---
UID: NS:dbghelp._IMAGEHLP_LINE64
title: "_IMAGEHLP_LINE64"
author: windows-sdk-content
description: Represents a source file line.
old-location: base\imagehlp_line64_str.htm
old-project: debug
ms.assetid: 62124983-8381-4eb4-94f6-220b844aca45
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PIMAGEHLP_LINE64, IMAGEHLP_LINE, IMAGEHLP_LINE structure, IMAGEHLP_LINE64, IMAGEHLP_LINE64 structure, IMAGEHLP_LINEW64, PIMAGEHLP_LINE64, PIMAGEHLP_LINE64 structure pointer, _IMAGEHLP_LINE64, _win32_imagehlp_line64_str, base.imagehlp_line64_str, dbghelp/IMAGEHLP_LINE64, dbghelp/IMAGEHLP_LINEW64, dbghelp/PIMAGEHLP_LINE64"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dbghelp.h
req.include-header: 
req.redist: DbgHelp.dll 5.1 or later
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IMAGEHLP_LINEW64 (Unicode) and IMAGEHLP_LINE64 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMAGEHLP_LINE64, *PIMAGEHLP_LINE64
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - IMAGEHLP_LINE64
 - IMAGEHLP_LINE64
 - IMAGEHLP_LINEW64
 - IMAGEHLP_LINE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _IMAGEHLP_LINE64 structure


## -description


Represents a source file line.


## -struct-fields




### -field SizeOfStruct

The size of the structure, in bytes. The caller must set this member to <code>sizeof(IMAGEHLP_LINE64)</code>.


### -field Key

This member is reserved for use by the operating system.


### -field LineNumber

The line number in the file.


### -field FileName

The name of the file, including the full path.


### -field Address

The address of the first instruction in the line.


## -remarks



This structure supersedes the <b>IMAGEHLP_LINE</b> structure. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>IMAGEHLP_LINE</b> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define IMAGEHLP_LINE IMAGEHLP_LINE64
#define PIMAGEHLP_LINE PIMAGEHLP_LINE64
#else
typedef struct _IMAGEHLP_LINE {
    DWORD    SizeOfStruct; 
    PVOID    Key; 
    DWORD    LineNumber; 
    PCHAR    FileName; 
    DWORD    Address; 
} IMAGEHLP_LINE, *PIMAGEHLP_LINE;

typedef struct _IMAGEHLP_LINEW {
    DWORD    SizeOfStruct; 
    PVOID    Key; 
    DWORD    LineNumber; 
    PCHAR    FileName; 
    DWORD64  Address; 
} IMAGEHLP_LINEW, *PIMAGEHLP_LINEW;
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a1dad8e0-cd85-41f7-b0e3-e359be94c0ac">SymGetLineFromAddr64</a>



<a href="https://msdn.microsoft.com/cb8870f6-1bae-40df-842e-ec3ca0167691">SymGetLineFromName64</a>



<a href="https://msdn.microsoft.com/82adafc3-1080-43bc-b343-eaf59bdef6cb">SymGetLineNext64</a>



<a href="https://msdn.microsoft.com/7f6d0f20-5dfa-4d6c-8551-1dbc3cc54176">SymGetLinePrev64</a>
 

 

