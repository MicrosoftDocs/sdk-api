---
UID: NF:winsvc.UnlockServiceDatabase
title: UnlockServiceDatabase function (winsvc.h)
description: Unlocks a service control manager database by releasing the specified lock.
helpviewer_keywords: ["UnlockServiceDatabase","UnlockServiceDatabase function","_win32_unlockservicedatabase","base.unlockservicedatabase","winsvc/UnlockServiceDatabase"]
old-location: base\unlockservicedatabase.htm
tech.root: security
ms.assetid: 3277d175-ab0b-43ce-965f-f8087d0124e4
ms.date: 12/05/2018
ms.keywords: UnlockServiceDatabase, UnlockServiceDatabase function, _win32_unlockservicedatabase, base.unlockservicedatabase, winsvc/UnlockServiceDatabase
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UnlockServiceDatabase
 - winsvc/UnlockServiceDatabase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - UnlockServiceDatabase
---

# UnlockServiceDatabase function


## -description

<p class="CCE_Message">[This function has no effect as of Windows Vista.]

Unlocks a service control manager database by releasing the specified lock.

## -parameters

### -param ScLock [in]

The lock, which is obtained from a previous call to the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-lockservicedatabase">LockServiceDatabase</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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

<a href="/windows/desktop/api/winsvc/nf-winsvc-lockservicedatabase">LockServiceDatabase</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicelockstatusa">QueryServiceLockStatus</a>



<a href="/windows/desktop/Services/service-configuration">Service Configuration</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>