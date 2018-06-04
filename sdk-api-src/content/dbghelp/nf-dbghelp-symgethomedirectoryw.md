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

# SymGetHomeDirectoryW function


## -description


Retrieves the home directory used by Dbghelp.


## -parameters




### -param type [in]

The directory to be retrieved. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="hdBase"></a><a id="hdbase"></a><a id="HDBASE"></a><dl>
<dt><b>hdBase</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The home directory.

</td>
</tr>
<tr>
<td width="40%"><a id="hdSrc"></a><a id="hdsrc"></a><a id="HDSRC"></a><dl>
<dt><b>hdSrc</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The source directory.

</td>
</tr>
<tr>
<td width="40%"><a id="hdSym"></a><a id="hdsym"></a><a id="HDSYM"></a><dl>
<dt><b>hdSym</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The symbol directory.

</td>
</tr>
</table>
 


### -param dir [out]

A pointer to a string that receives the directory.


### -param size [in]

The size of the output buffer, in characters.


## -returns



If the function succeeds, the return value is a pointer to the <i>dir</i> parameter.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/12e65054-c4d5-44b9-8597-b841cac012f5">SymSetHomeDirectory</a>
 

 

