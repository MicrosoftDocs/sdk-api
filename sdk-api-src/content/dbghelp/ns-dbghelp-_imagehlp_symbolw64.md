---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _IMAGEHLP_SYMBOLW64 structure


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
 

 

