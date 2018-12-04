---
UID: NF:imapi2.IDiscRecorder2.AcquireExclusiveAccess
title: IDiscRecorder2::AcquireExclusiveAccess
author: windows-sdk-content
description: Acquires exclusive access to the device.
old-location: imapi\idiscrecorder2_acquireexclusiveaccess.htm
tech.root: imapi
ms.assetid: 58cb5efa-74bc-4444-aa05-be41a6c63b3a
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: AcquireExclusiveAccess, AcquireExclusiveAccess method [IMAPI], AcquireExclusiveAccess method [IMAPI],IDiscRecorder2 interface, IDiscRecorder2 interface [IMAPI],AcquireExclusiveAccess method, IDiscRecorder2.AcquireExclusiveAccess, IDiscRecorder2::AcquireExclusiveAccess, imapi.idiscrecorder2_acquireexclusiveaccess, imapi2/IDiscRecorder2::AcquireExclusiveAccess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscRecorder2.AcquireExclusiveAccess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscRecorder2::AcquireExclusiveAccess


## -description


Acquires exclusive access to the device.


## -parameters




### -param force [in]

Set to VARIANT_TRUE to gain exclusive access to the volume whether the file system volume can or cannot be dismounted. If VARIANT_FALSE, this method  gains exclusive access only when there is no file system mounted on the volume.


### -param __MIDL__IDiscRecorder20000 [in]

String that contains the friendly name of the client application requesting exclusive access. Cannot be <b>NULL</b> or a zero-length string. The string must conform to the restrictions for the IOCTL_CDROM_EXCLUSIVE_ACCESS control code found in the DDK.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The device is currently being used by another application.

Value: 0x80070005

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_COMMAND_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The device failed to accept the command within the timeout period. This may be caused by the device having entered an inconsistent state, or the timeout value for the command may need to be increased.

Value: 0xC0AA020D

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_HANDLE)</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

Value: 6

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_DEV_NOT_EXIST)</b></dt>
</dl>
</td>
<td width="60%">
The specified network resource or device is no longer available.

Value: 55

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
The device associated with this recorder during the last operation has been exclusively locked, causing this operation to fail.

Value: 0xC0AA0210

</td>
</tr>
</table>
 




## -remarks



You should not have to call this method to acquire the lock yourself because the write operations, such as <a href="https://msdn.microsoft.com/9daf31f3-84c2-48b2-ab21-a3809b6ed9af">IDiscFormat2Data::Write</a>, acquires the lock for you.

Each recorder has a lock count. The first call to a recorder locks the device for exclusive access. Applications can use the <b>AcquireExclusiveAccess</b> method multiple times to apply multiple locks on a device. Each call increments the lock count by one. 

When unlocking a recorder, the lock count must reach zero to free the device for other clients. Calling the <a href="https://msdn.microsoft.com/940929d7-7940-448e-9554-3e3691772eb8">IDiscRecorder2::ReleaseExclusiveAccess</a> method decrements the lock count by one.

An equal number of calls to the  <b>AcquireExclusiveAccess</b> and <a href="https://msdn.microsoft.com/940929d7-7940-448e-9554-3e3691772eb8">ReleaseExclusiveAccess</a> methods are needed to free a device. Should the application exit unexpectedly or crash while holding the exclusive access, the CDROM.SYS driver will automatically release these exclusive locks.

If the device is already locked, you can call <a href="https://msdn.microsoft.com/32577b35-235a-4186-8fb3-18e5555cb56f">IDiscRecorder2::get_ExclusiveAccessOwner</a> to retrieve the name of the client application that currently has exclusive access.




## -see-also




<a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a>



<a href="https://msdn.microsoft.com/940929d7-7940-448e-9554-3e3691772eb8">IDiscRecorder2::ReleaseExclusiveAccess</a>



<a href="https://msdn.microsoft.com/32577b35-235a-4186-8fb3-18e5555cb56f">IDiscRecorder2::get_ExclusiveAccessOwner</a>
 

 

