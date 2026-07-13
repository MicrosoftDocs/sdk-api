---
UID: NF:winbase.SetMailslotInfo
title: SetMailslotInfo function (winbase.h)
description: Sets the time-out value used by the specified mailslot for a read operation.
helpviewer_keywords: ["MAILSLOT_WAIT_FOREVER","SetMailslotInfo","SetMailslotInfo function","_win32_setmailslotinfo","base.setmailslotinfo","winbase/SetMailslotInfo"]
old-location: base\setmailslotinfo.htm
tech.root: base
ms.assetid: 4afcbbfb-fd04-4813-b139-4baffc2fdf3c
ms.date: 12/05/2018
ms.keywords: MAILSLOT_WAIT_FOREVER, SetMailslotInfo, SetMailslotInfo function, _win32_setmailslotinfo, base.setmailslotinfo, winbase/SetMailslotInfo
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - SetMailslotInfo
 - winbase/SetMailslotInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - SetMailslotInfo
---

# SetMailslotInfo function


## -description

Sets the time-out value used by the specified mailslot for a read operation.

## -parameters

### -param hMailslot [in]

A handle to a mailslot. The 
<a href="/windows/desktop/api/winbase/nf-winbase-createmailslota">CreateMailslot</a> function must create this handle.

### -param lReadTimeout [in]

The time a read operation can wait for a message to be written to the mailslot before a time-out occurs, in milliseconds. The following values have special meanings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Returns immediately if no message is present. (The system does not treat an immediate return as an error.)

</td>
</tr>
<tr>
<td width="40%"><a id="MAILSLOT_WAIT_FOREVER"></a><a id="mailslot_wait_forever"></a><dl>
<dt><b>MAILSLOT_WAIT_FOREVER</b></dt>
<dt>((DWORD)-1)</dt>
</dl>
</td>
<td width="60%">
Waits forever for a message.

</td>
</tr>
</table>
 

This time-out value applies to all subsequent read operations and to all inherited mailslot handles.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The initial time-out value used by a mailslot for a read operation is typically set by 
<a href="/windows/desktop/api/winbase/nf-winbase-createmailslota">CreateMailslot</a> when the mailslot is created.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createmailslota">CreateMailslot</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getmailslotinfo">GetMailslotInfo</a>



<a href="/windows/desktop/ipc/mailslot-functions">Mailslot Functions</a>



<a href="/windows/desktop/ipc/mailslots">Mailslots Overview</a>