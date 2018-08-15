---
UID: NF:mbnapi.IMbnDeviceService.QueryCommand
title: IMbnDeviceService::QueryCommand
author: windows-sdk-content
description: Sends a QUERY control command to the device service of a Mobile Broadband device.
old-location: mbn\imbndeviceservice_querycommand.htm
old-project: mbn
ms.assetid: EA68206E-5656-4C83-AFB0-26E7F3692DE2
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnDeviceService interface [Microsoft Broadband Networks],QueryCommand method, IMbnDeviceService.QueryCommand, IMbnDeviceService::QueryCommand, QueryCommand, QueryCommand method [Microsoft Broadband Networks], QueryCommand method [Microsoft Broadband Networks],IMbnDeviceService interface, mbn.imbndeviceservice_querycommand, mbnapi/IMbnDeviceService::QueryCommand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnDeviceService.QueryCommand
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceService::QueryCommand


## -description


Sends a <b>QUERY</b> control command to the device service of a Mobile Broadband device.


## -parameters




### -param commandID [in]

An identifier for the command.


### -param deviceServiceData [in]

A byte array that is passed in to the device.


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
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered when executing this method.

</td>
</tr>
</table>
 




## -remarks



<b>QueryCommand</b> exists to implement vendor-specific device service functionality which is not otherwise covered in the Mobile Broadband API. The command session on a device service must be opened before the application can call <b>QueryCommand</b>.

The Mobile Broadband service will issue a <b>QUERY</b> request to the device. <i>deviceServiceData</i> will be copied byte-by-byte into the data buffer passed in to the request. This data buffer must not be more than <a href="https://msdn.microsoft.com/FCCE3CA1-ECD2-4964-952F-D4A077959519">MaxCommandSize</a> bytes.

This is an asynchronous operation and <b>QueryCommand</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/6A04FA3F-D5E4-4E02-A334-218A168762AB">OnQueryCommandComplete</a> method of the <a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/5C587408-DF03-4123-BA5A-C2CCC378F60A">IMbnDeviceService</a>
 

 

