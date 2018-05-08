---
UID: NF:imapi2.IDiscRecorder2.ReleaseExclusiveAccess
title: IDiscRecorder2::ReleaseExclusiveAccess
author: windows-driver-content
description: Releases exclusive access to the device.
old-location: imapi\idiscrecorder2_releaseexclusiveaccess.htm
old-project: imapi
ms.assetid: 940929d7-7940-448e-9554-3e3691772eb8
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IDiscRecorder2 interface [IMAPI],ReleaseExclusiveAccess method, IDiscRecorder2.ReleaseExclusiveAccess, IDiscRecorder2::ReleaseExclusiveAccess, ReleaseExclusiveAccess, ReleaseExclusiveAccess method [IMAPI], ReleaseExclusiveAccess method [IMAPI],IDiscRecorder2 interface, imapi.idiscrecorder2_releaseexclusiveaccess, imapi2/IDiscRecorder2::ReleaseExclusiveAccess
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
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IDiscRecorder2.ReleaseExclusiveAccess
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscRecorder2::ReleaseExclusiveAccess


## -description


Releases exclusive access to the device.


## -parameters






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
The device associated with this recorder during the last operation has been exclusively locked, causing this operation to failed.

Value: 0xC0AA0210

</td>
</tr>
</table>
 




## -remarks



Each recorder has a lock count. The first call to a recorder locks the device for exclusive access. Applications can use the <a href="https://msdn.microsoft.com/58cb5efa-74bc-4444-aa05-be41a6c63b3a">IDiscRecorder2::AcquireExclusiveAccess</a> method multiple times to apply multiple locks on a device. Each call increments the lock count by one.

When unlocking a recorder, the lock count must reach zero to free the device for other clients. Calling the <b>ReleaseExclusiveAccess</b> method decrements the lock count by one.

An equal number of  calls to the <a href="https://msdn.microsoft.com/58cb5efa-74bc-4444-aa05-be41a6c63b3a">AcquireExclusiveAccess</a> and <b>ReleaseExclusiveAccess</b> methods are needed to free a device. When the lock count reaches zero, recording device is free; the last lock has been removed.




## -see-also




<a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a>



<a href="https://msdn.microsoft.com/58cb5efa-74bc-4444-aa05-be41a6c63b3a">IDiscRecorder2::AcquireExclusiveAccess</a>



<a href="https://msdn.microsoft.com/32577b35-235a-4186-8fb3-18e5555cb56f">IDiscRecorder2::get_ExclusiveAccessOwner</a>
 

 

