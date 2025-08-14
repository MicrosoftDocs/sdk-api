---
UID: NF:winbase.GetCommConfig
title: GetCommConfig function (winbase.h)
description: Retrieves the current configuration of a communications device.
helpviewer_keywords: ["GetCommConfig","GetCommConfig function","_win32_getcommconfig","base.getcommconfig","winbase/GetCommConfig"]
old-location: base\getcommconfig.htm
tech.root: base
ms.assetid: 8c5b74f7-54e3-42c1-a111-a8ddfb677d4e
ms.date: 12/05/2018
ms.keywords: GetCommConfig, GetCommConfig function, _win32_getcommconfig, base.getcommconfig, winbase/GetCommConfig
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
 - GetCommConfig
 - winbase/GetCommConfig
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
 - GetCommConfig
---

# GetCommConfig function


## -description

Retrieves the current configuration of a communications device.

To retrieve the default configuration settings from the device manager, use the <a href="/windows/desktop/api/winbase/nf-winbase-getdefaultcommconfiga">GetDefaultCommConfig</a> function.

## -parameters

### -param hCommDev [in]

A handle to the open communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param lpCC [out]

A pointer to a buffer that receives a 
<a href="/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a> structure.

### -param lpdwSize [in, out]

The size, in bytes, of the buffer pointed to by <i>lpCC</i>. When the function returns, the variable contains the number of bytes copied if the function succeeds, or the number of bytes required if the buffer was too small.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getdefaultcommconfiga">GetDefaultCommConfig</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommconfig">SetCommConfig</a>