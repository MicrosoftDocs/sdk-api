---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

