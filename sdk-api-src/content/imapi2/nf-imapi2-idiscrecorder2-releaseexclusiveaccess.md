---
UID: NF:imapi2.IDiscRecorder2.ReleaseExclusiveAccess
title: IDiscRecorder2::ReleaseExclusiveAccess (imapi2.h)
description: Releases exclusive access to the device.
helpviewer_keywords: ["IDiscRecorder2 interface [IMAPI]","ReleaseExclusiveAccess method","IDiscRecorder2.ReleaseExclusiveAccess","IDiscRecorder2::ReleaseExclusiveAccess","ReleaseExclusiveAccess","ReleaseExclusiveAccess method [IMAPI]","ReleaseExclusiveAccess method [IMAPI]","IDiscRecorder2 interface","imapi.idiscrecorder2_releaseexclusiveaccess","imapi2/IDiscRecorder2::ReleaseExclusiveAccess"]
old-location: imapi\idiscrecorder2_releaseexclusiveaccess.htm
tech.root: imapi
ms.assetid: 940929d7-7940-448e-9554-3e3691772eb8
ms.date: 12/05/2018
ms.keywords: IDiscRecorder2 interface [IMAPI],ReleaseExclusiveAccess method, IDiscRecorder2.ReleaseExclusiveAccess, IDiscRecorder2::ReleaseExclusiveAccess, ReleaseExclusiveAccess, ReleaseExclusiveAccess method [IMAPI], ReleaseExclusiveAccess method [IMAPI],IDiscRecorder2 interface, imapi.idiscrecorder2_releaseexclusiveaccess, imapi2/IDiscRecorder2::ReleaseExclusiveAccess
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscRecorder2::ReleaseExclusiveAccess
 - imapi2/IDiscRecorder2::ReleaseExclusiveAccess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscRecorder2.ReleaseExclusiveAccess
---

# IDiscRecorder2::ReleaseExclusiveAccess


## -description

Releases exclusive access to the device.



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

Each recorder has a lock count. The first call to a recorder locks the device for exclusive access. Applications can use the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-acquireexclusiveaccess">IDiscRecorder2::AcquireExclusiveAccess</a> method multiple times to apply multiple locks on a device. Each call increments the lock count by one.

When unlocking a recorder, the lock count must reach zero to free the device for other clients. Calling the <b>ReleaseExclusiveAccess</b> method decrements the lock count by one.

An equal number of  calls to the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-acquireexclusiveaccess">AcquireExclusiveAccess</a> and <b>ReleaseExclusiveAccess</b> methods are needed to free a device. When the lock count reaches zero, recording device is free; the last lock has been removed.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-acquireexclusiveaccess">IDiscRecorder2::AcquireExclusiveAccess</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2-get_exclusiveaccessowner">IDiscRecorder2::get_ExclusiveAccessOwner</a>
