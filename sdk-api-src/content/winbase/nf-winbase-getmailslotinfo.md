---
UID: NF:winbase.GetMailslotInfo
title: GetMailslotInfo function (winbase.h)
description: Retrieves information about the specified mailslot.
helpviewer_keywords: ["GetMailslotInfo","GetMailslotInfo function","MAILSLOT_NO_MESSAGE","_win32_getmailslotinfo","base.getmailslotinfo","winbase/GetMailslotInfo"]
old-location: base\getmailslotinfo.htm
tech.root: base
ms.assetid: 873b4dbe-f808-4731-9314-a595ef7ef3c5
ms.date: 12/05/2018
ms.keywords: GetMailslotInfo, GetMailslotInfo function, MAILSLOT_NO_MESSAGE, _win32_getmailslotinfo, base.getmailslotinfo, winbase/GetMailslotInfo
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
 - GetMailslotInfo
 - winbase/GetMailslotInfo
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
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetMailslotInfo
---

# GetMailslotInfo function


## -description

Retrieves information about the specified mailslot.

## -parameters

### -param hMailslot [in]

A handle to a mailslot. The 
<a href="/windows/desktop/api/winbase/nf-winbase-createmailslota">CreateMailslot</a> function must create this handle.

### -param lpMaxMessageSize [out, optional]

The maximum message size, in bytes, allowed for this mailslot. This value can be greater than or equal to the value specified in the <i>cbMaxMsg</i> parameter of the 
<a href="/windows/desktop/api/winbase/nf-winbase-createmailslota">CreateMailslot</a> function that created the mailslot. This parameter can be <b>NULL</b>.

### -param lpNextSize [out, optional]

The size of the next message, in bytes. The following value has special meaning.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAILSLOT_NO_MESSAGE"></a><a id="mailslot_no_message"></a><dl>
<dt><b>MAILSLOT_NO_MESSAGE</b></dt>
<dt>((DWORD)-1)</dt>
</dl>
</td>
<td width="60%">
There is no next message.

</td>
</tr>
</table>
 

This parameter can be <b>NULL</b>.

### -param lpMessageCount [out, optional]

The total number of messages waiting to be read, when the function returns. This parameter can be <b>NULL</b>.

### -param lpReadTimeout [out, optional]

The amount of time, in milliseconds, a read operation can wait for a message to be written to the mailslot before a time-out occurs. This parameter is filled in when the function returns. This parameter can be <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createmailslota">CreateMailslot</a>



<a href="/windows/desktop/ipc/mailslot-functions">Mailslot Functions</a>



<a href="/windows/desktop/ipc/mailslots">Mailslots Overview</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setmailslotinfo">SetMailslotInfo</a>