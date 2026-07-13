---
UID: NF:winbase.SetCommBreak
title: SetCommBreak function (winbase.h)
description: Suspends character transmission for a specified communications device and places the transmission line in a break state until the ClearCommBreak function is called.
helpviewer_keywords: ["SetCommBreak","SetCommBreak function","_win32_setcommbreak","base.setcommbreak","winbase/SetCommBreak"]
old-location: base\setcommbreak.htm
tech.root: base
ms.assetid: 997fa1e0-c585-4517-abe7-77b9b08440ee
ms.date: 12/05/2018
ms.keywords: SetCommBreak, SetCommBreak function, _win32_setcommbreak, base.setcommbreak, winbase/SetCommBreak
req.header: winbase.h
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
 - SetCommBreak
 - winbase/SetCommBreak
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-comm-l1-1-2.dll
 - api-ms-win-core-comm-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetCommBreak
---

# SetCommBreak function


## -description

Suspends character transmission for a specified communications device and places the transmission line in a break state until the 
<a href="/windows/desktop/api/winbase/nf-winbase-clearcommbreak">ClearCommBreak</a> function is called.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-clearcommbreak">ClearCommBreak</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>