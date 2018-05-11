---
UID: NS:dbghelp._IMAGEHLP_SYMBOL64
title: "_IMAGEHLP_SYMBOL64"
author: windows-driver-content
description: Contains symbol information.
old-location: base\imagehlp_symbol64_str.htm
old-project: Debug
ms.assetid: 7b39281a-c34b-47ae-a3ff-5f0a7a66a588
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: "*PIMAGEHLP_SYMBOL64, IMAGEHLP_SYMBOL, IMAGEHLP_SYMBOL structure, IMAGEHLP_SYMBOL64, IMAGEHLP_SYMBOL64 structure, IMAGEHLP_SYMBOLW64, PIMAGEHLP_SYMBOL64, PIMAGEHLP_SYMBOL64 structure pointer, _IMAGEHLP_SYMBOL64, _win32_imagehlp_symbol64_str, base.imagehlp_symbol64_str, dbghelp/IMAGEHLP_SYMBOL64, dbghelp/IMAGEHLP_SYMBOLW64, dbghelp/PIMAGEHLP_SYMBOL64"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IMAGEHLP_SYMBOLW64 (Unicode) and IMAGEHLP_SYMBOL64 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMAGEHLP_SYMBOL64, *PIMAGEHLP_SYMBOL64
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	DbgHelp.h
api_name:
-	IMAGEHLP_SYMBOL64
-	IMAGEHLP_SYMBOL64
-	IMAGEHLP_SYMBOLW64
-	IMAGEHLP_SYMBOL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _IMAGEHLP_SYMBOL64 structure


## -description


Contains symbol information.


## -struct-fields




### -field SizeOfStruct

The size of the structure, in bytes. The caller must set this member to <code>sizeof(IMAGEHLP_SYMBOL64)</code>.


### -field Address

The virtual address for the symbol.


### -field Size

The size of the symbol, in bytes. This value is a best guess and can be zero.


### -field Flags

This member is reserved for use by the operating system.


### -field MaxNameLength

The maximum length of the string that the <b>Name</b> member can contain, in characters, not including the null-terminating character. Because symbol names can vary in length, this data structure is allocated by the caller. This member is used so the library knows how much memory is available for use by the symbol name.


### -field Name

The decorated or undecorated symbol name. If the buffer is not large enough for the complete name, it is truncated to <b>MaxNameLength</b> characters, including the null-terminating character.


## -remarks



This structure supersedes the <b>IMAGEHLP_SYMBOL</b> structure. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>IMAGEHLP_SYMBOL</b> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
 #define IMAGEHLP_SYMBOL IMAGEHLP_SYMBOL64
 #define PIMAGEHLP_SYMBOL PIMAGEHLP_SYMBOL64
#else
 typedef struct _IMAGEHLP_SYMBOL {
     DWORD SizeOfStruct; 
     DWORD Address; 
     DWORD Size; 
     DWORD Flags;  
     DWORD MaxNameLength; 
     CHAR  Name[1];  
 } IMAGEHLP_SYMBOL, *PIMAGEHLP_SYMBOL;
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c4882a3b-7773-4ab0-ad83-bdde512b5fb4">SymGetSymFromAddr64</a>



<a href="https://msdn.microsoft.com/9c9a1a57-06c2-422a-b078-5b7725d54bd4">SymGetSymFromName64</a>
 

 

