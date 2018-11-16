---
UID: NF:dbghelp.SymUnDName
title: SymUnDName function
author: windows-sdk-content
description: Undecorates a decorated C++ symbol name.
old-location: base\symundname64.htm
tech.root: Debug
ms.assetid: f7bea3a4-5e17-4743-894f-8eb8f9992cac
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SymUnDName, SymUnDName function, SymUnDName64, SymUnDName64 function, base.symundname64, dbghelp/SymUnDName, dbghelp/SymUnDName64
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymUnDName64
 - SymUnDName
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
- apiref
: 
- 
: 
- SymUnDName
: 
---

# SymUnDName function


## -description


Undecorates a decorated C++ symbol name.

Applications can also use the <a href="https://msdn.microsoft.com/f52e8e3b-3113-4d8c-b44a-846c574cfbd8">UnDecorateSymbolName</a> function.


## -parameters




### -param sym [in]

A pointer to an 
<a href="https://msdn.microsoft.com/7b39281a-c34b-47ae-a3ff-5f0a7a66a588">IMAGEHLP_SYMBOL64</a> structure that specifies the symbol to be undecorated.


### -param UnDecName [out]

A pointer to a buffer that receives the undecorated name.


### -param UnDecNameLength [in]

The size of the <i>UnDecName</i> buffer, in characters.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymUnDName</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymUnDName</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define SymUnDName SymUnDName64
#else
BOOL
IMAGEAPI
SymUnDName(
    __in PIMAGEHLP_SYMBOL sym,  
    __out_ecount(UnDecNameLength) PSTR UnDecName,   
    __in DWORD UnDecNameLength 
    );
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/f52e8e3b-3113-4d8c-b44a-846c574cfbd8">UnDecorateSymbolName</a>
 

 

