---
UID: NF:imapi2.IDiscRecorder2.DisableMcn
title: IDiscRecorder2::DisableMcn
author: windows-sdk-content
description: Disables Media Change Notification (MCN) for the device.
old-location: imapi\idiscrecorder2_disablemcn.htm
tech.root: imapi
ms.assetid: 3111863e-64bf-467c-ac73-7a16c9aeb3df
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DisableMcn, DisableMcn method [IMAPI], DisableMcn method [IMAPI],IDiscRecorder2 interface, IDiscRecorder2 interface [IMAPI],DisableMcn method, IDiscRecorder2.DisableMcn, IDiscRecorder2::DisableMcn, imapi.idiscrecorder2_disablemcn, imapi2/IDiscRecorder2::DisableMcn
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
 - IDiscRecorder2.DisableMcn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscRecorder2::DisableMcn


## -description


Disables Media Change Notification (MCN) for the device.


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



MCN is the CD-ROM device driver's method of detecting media change and state changes in the CD-ROM device. For example, when you change the media in a CD-ROM device, a MCN message is sent to trigger media features, such as Autoplay. To disable the features, call this method. 

To enable notifications, call the <a href="https://msdn.microsoft.com/ce848ba1-86b4-44cc-8f41-8b8eaba20521">IDiscRecorder2::EnableMcn</a> method. If the application crashes or closes unexpectedly, then MCN is automatically re-enabled by the driver.

Note that DisableMcn increments a reference count each time it is called. The <a href="https://msdn.microsoft.com/ce848ba1-86b4-44cc-8f41-8b8eaba20521">EnableMcn</a> method decrements the count. The device is enabled when the reference count is zero.




## -see-also




<a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a>



<a href="https://msdn.microsoft.com/ce848ba1-86b4-44cc-8f41-8b8eaba20521">IDiscRecorder2::EnableMcn</a>
 

 

