---
UID: NF:winsvc.LockServiceDatabase
title: LockServiceDatabase function
author: windows-driver-content
description: Requests ownership of the service control manager (SCM) database lock. Only one process can own the lock at any specified time.
old-location: base\lockservicedatabase.htm
old-project: Services
ms.assetid: 87861465-c966-479a-b906-27ae36cc83c8
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: LockServiceDatabase, LockServiceDatabase function, _win32_lockservicedatabase, base.lockservicedatabase, winsvc/LockServiceDatabase
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
api_name:
-	LockServiceDatabase
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LockServiceDatabase function


## -description


<p class="CCE_Message">[As of Windows Vista, this function is provided  for application compatibility and has no effect on the database.]

Requests ownership of the service control manager (SCM) database lock. Only one process can own the lock at any specified time.


## -parameters




### -param hSCManager [in]

A handle to the SCM database. This handle is returned by the 
<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a> function, and must have the <b>SC_MANAGER_LOCK</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is a lock to the specified SCM database.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes can be set by the SCM. Other error codes can be set by registry functions that are called by the SCM.

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
The handle does not have the <b>SC_MANAGER_LOCK</b> access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DATABASE_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
The database is locked.

</td>
</tr>
</table>
 




## -remarks



A lock is a protocol used by setup and configuration programs and the SCM to serialize access to the service tree in the registry. The only time the SCM requests ownership of the lock is when it is starting a service.

A program that acquires the SCM database lock and fails to release it prevents the SCM from starting other services. Because of the severity of this issue, processes are no longer allowed to lock the database. For compatibility with older applications, the <b>LockServiceDatabase</b> function returns a lock but has no other effect. 

<b>Windows Server 2003 and Windows XP:  </b>Acquiring the SCM database lock prevents the SCM from starting a service until the lock is released. For example, a program that must configure several related services before any of them starts could call 
<b>LockServiceDatabase</b> before configuring the first service. Alternatively, it could ensure that none of the services are started until the configuration has been completed.

A call to the 
<a href="https://msdn.microsoft.com/f185a878-e1c3-4fe5-8ec9-c5296d27f985">StartService</a> function to start a service in a locked database fails. No other SCM functions are affected by a lock.

The lock is held until the <b>SC_LOCK</b> handle is specified in a subsequent call to the 
<a href="https://msdn.microsoft.com/3277d175-ab0b-43ce-965f-f8087d0124e4">UnlockServiceDatabase</a> function. If a process that owns a lock terminates, the SCM automatically cleans up and releases ownership of the lock. 

Failing to release the lock can cause system problems. A process that acquires  the lock should release it as soon as possible. 






## -see-also




<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a>



<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a>



<a href="https://msdn.microsoft.com/5139d31b-65f1-41ba-852a-91eab1dc366e">QueryServiceLockStatus</a>



<a href="https://msdn.microsoft.com/fc8c631e-076c-4745-8db0-90f46a202e6a">Service Configuration</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>



<a href="https://msdn.microsoft.com/39481d9a-79d5-4bbf-8480-4095a34dddb6">SetServiceObjectSecurity</a>



<a href="https://msdn.microsoft.com/f185a878-e1c3-4fe5-8ec9-c5296d27f985">StartService</a>



<a href="https://msdn.microsoft.com/3277d175-ab0b-43ce-965f-f8087d0124e4">UnlockServiceDatabase</a>
 

 

