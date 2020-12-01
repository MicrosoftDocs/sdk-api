---
UID: NF:winbase.GetNumaNodeNumberFromHandle
title: GetNumaNodeNumberFromHandle function (winbase.h)
description: Retrieves the NUMA node associated with the file or I/O device represented by the specified file handle.
helpviewer_keywords: ["GetNumaNodeNumberFromHandle","GetNumaNodeNumberFromHandle function","base.getnumanodenumberfromhandle","winbase/GetNumaNodeNumberFromHandle"]
old-location: base\getnumanodenumberfromhandle.htm
tech.root: backup
ms.assetid: 7622f7c9-2dfc-4ab7-b3e9-48d483c6cc0e
ms.date: 12/05/2018
ms.keywords: GetNumaNodeNumberFromHandle, GetNumaNodeNumberFromHandle function, base.getnumanodenumberfromhandle, winbase/GetNumaNodeNumberFromHandle
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - GetNumaNodeNumberFromHandle
 - winbase/GetNumaNodeNumberFromHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
api_name:
 - GetNumaNodeNumberFromHandle
---

# GetNumaNodeNumberFromHandle function


## -description

Retrieves the NUMA node associated with the file or I/O device represented by the specified file handle.

## -parameters

### -param hFile [in]

A handle to a file or I/O device. Examples of I/O devices include files, file streams, volumes, physical disks, and sockets. For more information, see the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -param NodeNumber [out]

A pointer to a variable to receive the number of the NUMA node associated with the specified file handle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the specified handle does not have a node associated with it, the function returns FALSE. The value of the <i>NodeNumber</i> parameter is undetermined and should not be used.

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>