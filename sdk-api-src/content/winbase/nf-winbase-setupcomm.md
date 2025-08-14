---
UID: NF:winbase.SetupComm
title: SetupComm function (winbase.h)
description: Initializes the communications parameters for a specified communications device.
helpviewer_keywords: ["SetupComm","SetupComm function","_win32_setupcomm","base.setupcomm","winbase/SetupComm"]
old-location: base\setupcomm.htm
tech.root: base
ms.assetid: 7b42fdad-5847-4036-957e-2f71ad982d9f
ms.date: 12/05/2018
ms.keywords: SetupComm, SetupComm function, _win32_setupcomm, base.setupcomm, winbase/SetupComm
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
 - SetupComm
 - winbase/SetupComm
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
 - SetupComm
---

# SetupComm function


## -description

Initializes the communications parameters for a specified communications device.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param dwInQueue [in]

The recommended size of the device's internal input buffer, in bytes.

### -param dwOutQueue [in]

The recommended size of the device's internal output buffer, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After a process uses the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function to open a handle to a communications device, but before doing any I/O with the device, it can call 
<b>SetupComm</b> to set the communications parameters for the device. If it does not set them, the device uses the default parameters when the first call to another communications function occurs.

The <i>dwInQueue</i> and <i>dwOutQueue</i> parameters specify the recommended sizes for the internal buffers used by the driver for the specified device. For example, YMODEM protocol packets are slightly larger than 1024 bytes. Therefore, a recommended buffer size might be 1200 bytes for YMODEM communications. For Ethernet-based communications, a recommended buffer size might be 1600 bytes, which is slightly larger than a single Ethernet frame.

The device driver receives the recommended buffer sizes, but is free to use any input and output (I/O) buffering scheme, as long as it provides reasonable performance and data is not lost due to overrun (except under extreme circumstances). For example, the function can succeed even though the driver does not allocate a buffer, as long as some other portion of the system provides equivalent functionality.

## -see-also

<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommstate">SetCommState</a>