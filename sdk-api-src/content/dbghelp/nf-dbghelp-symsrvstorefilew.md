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

# SymSrvStoreFileW function


## -description


Stores a file in the specified symbol store.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param SrvPath [in, optional]

The symbol store.


### -param File [in]

The name of the file.


### -param Flags [in]

The flags that control the function. 
This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYMSTOREOPT_COMPRESS"></a><a id="symstoreopt_compress"></a><dl>
<dt><b>SYMSTOREOPT_COMPRESS</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Compress the file.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMSTOREOPT_OVERWRITE"></a><a id="symstoreopt_overwrite"></a><dl>
<dt><b>SYMSTOREOPT_OVERWRITE</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Overwrite the file if it exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMSTOREOPT_PASS_IF_EXISTS"></a><a id="symstoreopt_pass_if_exists"></a><dl>
<dt><b>SYMSTOREOPT_PASS_IF_EXISTS</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
Do not report an error if the file already exists in the symbol store.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMSTOREOPT_POINTER"></a><a id="symstoreopt_pointer"></a><dl>
<dt><b>SYMSTOREOPT_POINTER</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
Store in File.ptr.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMSTOREOPT_RETURNINDEX"></a><a id="symstoreopt_returnindex"></a><dl>
<dt><b>SYMSTOREOPT_RETURNINDEX</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Return the index only.

</td>
</tr>
</table>
 


## -returns




						If the function succeeds, the return value is a pointer to a null-terminated string that specifies the full-qualified path to the stored file.
						

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>
 

 

