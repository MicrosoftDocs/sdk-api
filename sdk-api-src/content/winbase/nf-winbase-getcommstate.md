---
UID: NF:winbase.GetCommState
title: GetCommState function (winbase.h)
description: Retrieves the current control settings for a specified communications device.
helpviewer_keywords: ["GetCommState","GetCommState function","_win32_getcommstate","base.getcommstate","winbase/GetCommState"]
old-location: base\getcommstate.htm
tech.root: base
ms.assetid: 974c2ddc-9f7f-445e-ac47-8cd86817ce9b
ms.date: 12/05/2018
ms.keywords: GetCommState, GetCommState function, _win32_getcommstate, base.getcommstate, winbase/GetCommState
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
 - GetCommState
 - winbase/GetCommState
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
 - GetCommState
---

# GetCommState function


## -description

Retrieves the current control settings for a specified communications device.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param lpDCB [in, out]

A pointer to a 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure that receives the control settings information.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommstate">SetCommState</a>