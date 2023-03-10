---
UID: NF:winbase.FatalExit
title: FatalExit function (winbase.h)
description: Transfers execution control to the debugger. The behavior of the debugger thereafter is specific to the type of debugger used.
helpviewer_keywords: ["FatalExit","FatalExit function","_win32_fatalexit","base.fatalexit","winbase/FatalExit"]
old-location: base\fatalexit.htm
tech.root: Debug
ms.assetid: 6015e025-872f-455a-89f9-0ff96e59ef15
ms.date: 12/05/2018
ms.keywords: FatalExit, FatalExit function, _win32_fatalexit, base.fatalexit, winbase/FatalExit
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FatalExit
 - winbase/FatalExit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - FatalExit
---

# FatalExit function


## -description

Transfers execution control to the debugger. The behavior of the debugger thereafter is specific to the type of debugger used.

## -parameters

### -param ExitCode [in]

The error code associated with the exit.

## -returns

This function does not return a value.

## -remarks

An application should only use 
<b>FatalExit</b> for debugging purposes. It should not call the function in a retail version of the application because doing so will terminate the application.

## -see-also

<a href="/windows/desktop/Debug/communicating-with-the-debugger">Communicating with the Debugger</a>



<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-fatalexit">FatalAppExit</a>