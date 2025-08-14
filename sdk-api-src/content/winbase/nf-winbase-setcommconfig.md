---
UID: NF:winbase.SetCommConfig
title: SetCommConfig function (winbase.h)
description: Sets the current configuration of a communications device.
helpviewer_keywords: ["SetCommConfig","SetCommConfig function","_win32_setcommconfig","base.setcommconfig","winbase/SetCommConfig"]
old-location: base\setcommconfig.htm
tech.root: base
ms.assetid: e38be757-81c6-49ae-8d90-4387893e8ec5
ms.date: 12/05/2018
ms.keywords: SetCommConfig, SetCommConfig function, _win32_setcommconfig, base.setcommconfig, winbase/SetCommConfig
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
 - SetCommConfig
 - winbase/SetCommConfig
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
 - SetCommConfig
---

# SetCommConfig function


## -description

Sets the current configuration of a communications device.

## -parameters

### -param hCommDev [in]

A handle to the open communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param lpCC [in]

A pointer to a 
<a href="/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a> structure.

### -param dwSize [in]

The size of the structure pointed to by <i>lpCC</i>, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getcommconfig">GetCommConfig</a>