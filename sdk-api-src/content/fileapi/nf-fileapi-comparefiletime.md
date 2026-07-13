---
UID: NF:fileapi.CompareFileTime
title: CompareFileTime function (fileapi.h)
description: Compares two file times.
helpviewer_keywords: ["CompareFileTime","CompareFileTime function","_win32_comparefiletime","base.comparefiletime","fileapi/CompareFileTime","winbase/CompareFileTime"]
old-location: base\comparefiletime.htm
tech.root: winprog
ms.assetid: 38161826-3a43-42a3-a49d-415b5f7451c5
ms.date: 12/05/2018
ms.keywords: CompareFileTime, CompareFileTime function, _win32_comparefiletime, base.comparefiletime, fileapi/CompareFileTime, winbase/CompareFileTime
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - CompareFileTime
 - fileapi/CompareFileTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CompareFileTime
---

# CompareFileTime function


## -description

Compares two file times.

## -parameters

### -param lpFileTime1 [in]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the 
     first file time.

### -param lpFileTime2 [in]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the 
     second file time.

## -returns

The return value is one of the following values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
First file time is earlier than second file time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
First file time is equal to second file time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
First file time is later than second file time.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/SysInfo/file-times">File Times</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfiletime">GetFileTime</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>