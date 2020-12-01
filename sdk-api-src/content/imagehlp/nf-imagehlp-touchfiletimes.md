---
UID: NF:imagehlp.TouchFileTimes
title: TouchFileTimes function (imagehlp.h)
description: Updates the date and time at which the specified file was last modified.
helpviewer_keywords: ["TouchFileTimes","TouchFileTimes function","_win32_touchfiletimes","base.touchfiletimes","imagehlp/TouchFileTimes"]
old-location: base\touchfiletimes.htm
tech.root: Debug
ms.assetid: add84ca7-2497-4859-bc69-270ad493a08a
ms.date: 12/05/2018
ms.keywords: TouchFileTimes, TouchFileTimes function, _win32_touchfiletimes, base.touchfiletimes, imagehlp/TouchFileTimes
req.header: imagehlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imagehlp.lib
req.dll: Imagehlp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TouchFileTimes
 - imagehlp/TouchFileTimes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imagehlp.dll
api_name:
 - TouchFileTimes
---

# TouchFileTimes function


## -description

Updates the date and time at which the specified file was last modified.

## -parameters

### -param FileHandle [in]

A handle to the file of interest.

### -param pSystemTime [in]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure. If this parameter is <b>NULL</b>, the current system date and time is used.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/image-help-library">Image Help Library Overview</a>



<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>