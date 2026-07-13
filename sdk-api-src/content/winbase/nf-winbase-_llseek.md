---
UID: NF:winbase._llseek
title: _llseek function (winbase.h)
description: Repositions the file pointer for the specified file.
helpviewer_keywords: ["_llseek","_llseek function [Windows API]","winbase/_llseek","winprog._llseek"]
old-location: winprog\_llseek.htm
tech.root: winprog
ms.assetid: 1861bd5a-97e6-463d-9586-22458a1d9210
ms.date: 12/05/2018
ms.keywords: _llseek, _llseek function [Windows API], winbase/_llseek, winprog._llseek
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _llseek
 - winbase/_llseek
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-private-l1-2-0.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Private-l1-1-2.dll
api_name:
 - _llseek
---

# _llseek function


## -description

<p class="CCE_Message">[This function is provided for compatibility with 16-bit versions of Windows. New applications should use the <b>SetFilePointer</b> function.]

Repositions the file pointer for the specified file.

## -parameters

### -param hFile

A handle to an open file. This handle is created by <a href="/windows/win32/api/winbase/nf-winbase-_lcreat">_lcreat</a>.

### -param lOffset

The number of bytes that the file pointer is to be moved.

### -param iOrigin

The starting point and the direction that the pointer will be moved.


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
Moves the pointer from the beginning of the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Moves the file from its current location.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Moves the pointer from the end of the file.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value specifies the new offset. Otherwise, the return value is HFILE_ERROR. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

When a file is initially opened, the file pointer is set to the beginning of the file. The <b>_llseek</b> function moves the pointer without reading data, which allows random access to the content of the file.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-setfilepointer">SetFilePointer</a>