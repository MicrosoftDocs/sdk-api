---
UID: NF:winsvc.QueryServiceLockStatusA
title: QueryServiceLockStatusA function
author: windows-sdk-content
description: Retrieves the lock status of the specified service control manager database.
old-location: base\queryservicelockstatus.htm
old-project: Services
ms.assetid: 5139d31b-65f1-41ba-852a-91eab1dc366e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: QueryServiceLockStatus, QueryServiceLockStatus function, QueryServiceLockStatusA, QueryServiceLockStatusW, _win32_queryservicelockstatus, base.queryservicelockstatus, winsvc/QueryServiceLockStatus, winsvc/QueryServiceLockStatusA, winsvc/QueryServiceLockStatusW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsvc.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryServiceLockStatusW (Unicode) and QueryServiceLockStatusA (ANSI)
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
 - QueryServiceLockStatus
 - QueryServiceLockStatusA
 - QueryServiceLockStatusW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# QueryServiceLockStatusA function


## -description


<p class="CCE_Message">[This function has  no effect as of Windows Vista.]

Retrieves the lock status of the specified service control manager database.


## -parameters




### -param hSCManager [in]

A handle to the service control manager database. The 
<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a> function returns this handle, which must have the SC_MANAGER_QUERY_LOCK_STATUS access right. For more information, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>.


### -param lpLockStatus [out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/de9797b7-02b0-43cb-bed3-50b7e8676f36">QUERY_SERVICE_LOCK_STATUS</a> structure that receives the lock status of the specified database is returned, plus the strings to which its members point.


### -param cbBufSize [in]

The size of the buffer pointed to by the <i>lpLockStatus</i> parameter, in bytes.


### -param pcbBytesNeeded [out]

A pointer to a variable that receives the number of bytes needed to return all the lock status information, if the function fails.


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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The handle does not have the SC_MANAGER_QUERY_LOCK_STATUS access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
There is more lock status information than would fit into the <i>lpLockStatus</i> buffer. The number of bytes required to get all the information is returned in the <i>pcbBytesNeeded</i> parameter. Nothing is written to <i>lpLockStatus</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
</table>
 




## -remarks



The 
<b>QueryServiceLockStatus</b> function returns a 
<a href="https://msdn.microsoft.com/de9797b7-02b0-43cb-bed3-50b7e8676f36">QUERY_SERVICE_LOCK_STATUS</a> structure that indicates whether the specified database is locked. If the database is locked, the structure provides the account name of the user that owns the lock and the length of time that the lock has been held.

A process calls the 
<a href="https://msdn.microsoft.com/87861465-c966-479a-b906-27ae36cc83c8">LockServiceDatabase</a> function to acquire ownership of a service control manager database lock and the 
<a href="https://msdn.microsoft.com/3277d175-ab0b-43ce-965f-f8087d0124e4">UnlockServiceDatabase</a> function to release the lock.




## -see-also




<a href="https://msdn.microsoft.com/87861465-c966-479a-b906-27ae36cc83c8">LockServiceDatabase</a>



<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a>



<a href="https://msdn.microsoft.com/de9797b7-02b0-43cb-bed3-50b7e8676f36">QUERY_SERVICE_LOCK_STATUS</a>



<a href="https://msdn.microsoft.com/fc8c631e-076c-4745-8db0-90f46a202e6a">Service Configuration</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>



<a href="https://msdn.microsoft.com/3277d175-ab0b-43ce-965f-f8087d0124e4">UnlockServiceDatabase</a>
 

 

