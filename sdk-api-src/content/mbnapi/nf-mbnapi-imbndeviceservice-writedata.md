---
UID: NF:mbnapi.IMbnDeviceService.WriteData
title: IMbnDeviceService::WriteData (mbnapi.h)
author: windows-sdk-content
description: Write data to a device service data session.
old-location: mbn\imbndeviceservice_writedata.htm
tech.root: mbn
ms.assetid: D2CD630B-FCD5-485D-84A6-B2A942842A1F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnDeviceService interface [Microsoft Broadband Networks],WriteData method, IMbnDeviceService.WriteData, IMbnDeviceService::WriteData, WriteData, WriteData method [Microsoft Broadband Networks], WriteData method [Microsoft Broadband Networks],IMbnDeviceService interface, mbn.imbndeviceservice_writedata, mbnapi/IMbnDeviceService::WriteData
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnDeviceService.WriteData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnDeviceService::WriteData


## -description


Write data to a device service data session.


## -parameters




### -param deviceServiceData [in]

A byte array that is passed in to the device to write.


### -param requestID [out]

A unique request ID assigned by the Mobile Broadband service to identify this request.


## -returns



The method can return one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This device service command is not allowed for calling process privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_BUFFER_OVERFLOW)</b></dt>
</dl>
</td>
<td width="60%">
The length of the <i>deviceServiceData</i> is greater than the supported <a href="https://msdn.microsoft.com/E6E29974-083D-4EC8-A4FF-5AACE7435444">MaxDataSize</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_OPEN_FAILED)</b></dt>
</dl>
</td>
<td width="60%">
The device service session is not open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered when executing this method.

</td>
</tr>
</table>
 




## -remarks



<b>WriteData</b> passes a bulk data to a vendor-specific device service on the device. The Mobile Broadband service will forward this request to the device. <i>deviceServiceData</i> will be copied byte-by-byte into the data buffer passed in to the request. This data buffer must be less than <a href="https://msdn.microsoft.com/E6E29974-083D-4EC8-A4FF-5AACE7435444">MaxDataSize</a> bytes.

The data session must be opened before the application can call <b>WriteData</b>. The operating system does not provide guarantees on the latency or performance of <b>WriteData</b>.

This is an asynchronous operation and <b>WriteData</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/2C885E15-C689-4ADF-BFB0-24D03932FAC7">OnWriteDataComplete</a> method of the <a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/5C587408-DF03-4123-BA5A-C2CCC378F60A">IMbnDeviceService</a>
 

 

