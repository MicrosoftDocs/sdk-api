---
UID: NF:winbase._lcreat
title: "_lcreat function"
author: windows-sdk-content
description: Creates or opens the specified file.
old-location: winprog\_lcreat.htm
old-project: DevNotes
ms.assetid: 89e19823-c720-4bfc-95d5-18942573dd94
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: "_lcreat, _lcreat function [Windows API], winbase/_lcreat, winprog._lcreat"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-2.dll
api_name:
 - _lcreat
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# _lcreat function


## -description


<p class="CCE_Message">[This function is provided for compatibility with 16-bit versions of Windows. New applications should use the <b>CreateFile</b> function.]

Creates or opens the specified file. This documentation is included only for troubleshooting existing code.


## -parameters




### -param lpPathName

TBD


### -param iAttribute

TBD




#### - fnAttribute

The attributes of the file.


This parameter must be set to one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Normal. Can be read from or written to without restriction.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Read-only. Cannot be opened for write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Hidden. Not found by directory search.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
System. Not found by directory search.

</td>
</tr>
</table>
 


#### - lpszFileName

The name of the file. The string must consist of characters from the Windows ANSI character set.


## -returns



If the function succeeds, the return value is a file handle. Otherwise, the return value is HFILE_ERROR. To get extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



If the file does not exist, <b>_lcreat</b> creates and opens a new file for writing. If the file does exist, <b>_lcreat</b> truncates the file size to zero and opens it for reading and writing.

When the function opens a file, the pointer is set to the beginning of the file.

Use the <b>_lcreat</b> function with care. It can open any file, even one already opened by another function.




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>
 

 

