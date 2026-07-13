---
UID: NF:winbase.TransmitCommChar
title: TransmitCommChar function (winbase.h)
description: Transmits a specified character ahead of any pending data in the output buffer of the specified communications device.
helpviewer_keywords: ["TransmitCommChar","TransmitCommChar function","_win32_transmitcommchar","base.transmitcommchar","winbase/TransmitCommChar"]
old-location: base\transmitcommchar.htm
tech.root: base
ms.assetid: 599c3d04-6cd3-41ac-88a8-752f4b83d46b
ms.date: 12/05/2018
ms.keywords: TransmitCommChar, TransmitCommChar function, _win32_transmitcommchar, base.transmitcommchar, winbase/TransmitCommChar
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
 - TransmitCommChar
 - winbase/TransmitCommChar
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
 - TransmitCommChar
---

# TransmitCommChar function


## -description

Transmits a specified character ahead of any pending data in the output buffer of the specified communications device.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param cChar [in]

The character to be transmitted.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>TransmitCommChar</b> function is useful for sending an interrupt character (such as a CTRL+C) to a host system.

If the device is not transmitting, 
<b>TransmitCommChar</b> cannot be called repeatedly. Once 
<b>TransmitCommChar</b> places a character in the output buffer, the character must be transmitted before the function can be called again. If the previous character has not yet been sent, 
<b>TransmitCommChar</b> returns an error.

## -see-also

<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-waitcommevent">WaitCommEvent</a>