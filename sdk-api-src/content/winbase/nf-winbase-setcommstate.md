---
UID: NF:winbase.SetCommState
title: SetCommState function (winbase.h)
description: Configures a communications device according to the specifications in a device-control block (a DCB structure). The function reinitializes all hardware and control settings, but it does not empty output or input queues.
helpviewer_keywords: ["SetCommState","SetCommState function","_win32_setcommstate","base.setcommstate","winbase/SetCommState"]
old-location: base\setcommstate.htm
tech.root: base
ms.assetid: a9296514-4789-4830-ba68-84a16ac7fc47
ms.date: 12/05/2018
ms.keywords: SetCommState, SetCommState function, _win32_setcommstate, base.setcommstate, winbase/SetCommState
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
 - SetCommState
 - winbase/SetCommState
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
 - SetCommState
---

# SetCommState function


## -description

Configures a communications device according to the specifications in a device-control block (a 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure). The function reinitializes all hardware and control settings, but it does not empty output or input queues.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param lpDCB [in]

A pointer to a 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure that contains the configuration information for the specified communications device.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SetCommState</b> function uses a 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure to specify the desired configuration. The 
<a href="/windows/desktop/api/winbase/nf-winbase-getcommstate">GetCommState</a> function returns the current configuration.

To set only a few members of the 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure, you should modify a 
<b>DCB</b> structure that has been filled in by a call to 
<a href="/windows/desktop/api/winbase/nf-winbase-getcommstate">GetCommState</a>. This ensures that the other members of the 
<b>DCB</b> structure have appropriate values.

The 
<b>SetCommState</b> function fails if the <b>XonChar</b> member of the 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure is equal to the <b>XoffChar</b> member.

When 
<b>SetCommState</b> is used to configure the 8250, the following restrictions apply to the values for the 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure's <b>ByteSize</b> and <b>StopBits</b> members:

The number of data bits must be 5 to 8 bits.


#### Examples

For an example, see 
<a href="/windows/desktop/DevIO/configuring-a-communications-resource">Configuring a Communications Resource</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-buildcommdcba">BuildCommDCB</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getcommstate">GetCommState</a>