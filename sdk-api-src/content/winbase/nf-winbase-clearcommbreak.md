---
UID: NF:winbase.ClearCommBreak
title: ClearCommBreak function (winbase.h)
description: Restores character transmission for a specified communications device and places the transmission line in a nonbreak state.
helpviewer_keywords: ["ClearCommBreak","ClearCommBreak function","_win32_clearcommbreak","base.clearcommbreak","winbase/ClearCommBreak"]
old-location: base\clearcommbreak.htm
tech.root: base
ms.assetid: 9692242c-e209-4492-ab0b-333f09595597
ms.date: 12/05/2018
ms.keywords: ClearCommBreak, ClearCommBreak function, _win32_clearcommbreak, base.clearcommbreak, winbase/ClearCommBreak
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
 - ClearCommBreak
 - winbase/ClearCommBreak
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
 - ClearCommBreak
---

# ClearCommBreak function


## -description

Restores character transmission for a specified communications device and places the transmission line in a nonbreak state.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A communications device is placed in a break state by the 
<a href="/windows/desktop/api/winbase/nf-winbase-setcommbreak">SetCommBreak</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-escapecommfunction">EscapeCommFunction</a> function. Character transmission is then suspended until the break state is cleared by calling 
<b>ClearCommBreak</b>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-clearcommerror">ClearCommError</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-escapecommfunction">EscapeCommFunction</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommbreak">SetCommBreak</a>