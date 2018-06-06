---
UID: NF:winsvc.UnlockServiceDatabase
title: UnlockServiceDatabase function
author: windows-sdk-content
description: Unlocks a service control manager database by releasing the specified lock.
old-location: base\unlockservicedatabase.htm
old-project: Services
ms.assetid: 3277d175-ab0b-43ce-965f-f8087d0124e4
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: UnlockServiceDatabase, UnlockServiceDatabase function, _win32_unlockservicedatabase, base.unlockservicedatabase, winsvc/UnlockServiceDatabase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - UnlockServiceDatabase
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# UnlockServiceDatabase function


## -description


<p class="CCE_Message">[This function has no effect as of Windows Vista.]

Unlocks a service control manager database by releasing the specified lock.


## -parameters




### -param ScLock [in]

The lock, which is obtained from a previous call to the 
<a href="https://msdn.microsoft.com/87861465-c966-479a-b906-27ae36cc83c8">LockServiceDatabase</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes can be set by the service control manager. Other error codes can be set by the registry functions that are called by the service control manager.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SERVICE_LOCK</b></dt>
</dl>
</td>
<td width="60%">
The specified lock is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/87861465-c966-479a-b906-27ae36cc83c8">LockServiceDatabase</a>



<a href="https://msdn.microsoft.com/5139d31b-65f1-41ba-852a-91eab1dc366e">QueryServiceLockStatus</a>



<a href="https://msdn.microsoft.com/fc8c631e-076c-4745-8db0-90f46a202e6a">Service Configuration</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>
 

 

