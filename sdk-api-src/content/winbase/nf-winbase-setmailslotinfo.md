---
UID: NF:winbase.SetMailslotInfo
title: SetMailslotInfo function
author: windows-sdk-content
description: Sets the time-out value used by the specified mailslot for a read operation.
old-location: base\setmailslotinfo.htm
old-project: ipc
ms.assetid: 4afcbbfb-fd04-4813-b139-4baffc2fdf3c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: MAILSLOT_WAIT_FOREVER, SetMailslotInfo, SetMailslotInfo function, _win32_setmailslotinfo, base.setmailslotinfo, winbase/SetMailslotInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetMailslotInfo function


## -description


Sets the time-out value used by the specified mailslot for a read operation.


## -parameters




### -param hMailslot [in]

A handle to a mailslot. The 
<a href="https://msdn.microsoft.com/a2e8199f-4d00-4315-9562-ff30f4fafcb7">CreateMailslot</a> function must create this handle.


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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The initial time-out value used by a mailslot for a read operation is typically set by 
<a href="https://msdn.microsoft.com/a2e8199f-4d00-4315-9562-ff30f4fafcb7">CreateMailslot</a> when the mailslot is created.




## -see-also




<a href="https://msdn.microsoft.com/a2e8199f-4d00-4315-9562-ff30f4fafcb7">CreateMailslot</a>



<a href="https://msdn.microsoft.com/873b4dbe-f808-4731-9314-a595ef7ef3c5">GetMailslotInfo</a>



<a href="https://msdn.microsoft.com/85f89fcc-2ab1-411b-ab3e-f1e9d425433f">Mailslot Functions</a>



<a href="https://msdn.microsoft.com/e23894ca-edc7-49e6-bcc4-c82f357ecedf">Mailslots Overview</a>
 

 

