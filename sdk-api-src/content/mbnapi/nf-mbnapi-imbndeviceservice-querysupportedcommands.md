---
UID: NF:mbnapi.IMbnDeviceService.QuerySupportedCommands
title: IMbnDeviceService::QuerySupportedCommands method
author: windows-driver-content
description: Gets the list of commands IDs supported by the Mobile Broadband device service.
old-location: mbn\imbndeviceservice_querysupportedcommands.htm
old-project: mbn
ms.assetid: E82AAD40-1E91-449D-8F1C-CE31B394B2DF
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnDeviceService, IMbnDeviceService interface [Microsoft Broadband Networks], QuerySupportedCommands method, IMbnDeviceService::QuerySupportedCommands, QuerySupportedCommands method [Microsoft Broadband Networks], QuerySupportedCommands method [Microsoft Broadband Networks], IMbnDeviceService interface, QuerySupportedCommands,IMbnDeviceService.QuerySupportedCommands, mbn.imbndeviceservice_querysupportedcommands, mbnapi/IMbnDeviceService::QuerySupportedCommands
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnDeviceService.QuerySupportedCommands
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceService::QuerySupportedCommands method


## -description


Gets the list of commands IDs supported by the Mobile Broadband device service.


## -parameters




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



<b>QuerySupportedCommands</b> enables the application to enumerate the list of command messages supported by a device service on the Mobile Broadband device. 

This is an asynchronous operation and <b>QuerySupportedCommands</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/CA304FF5-B630-4CD5-8E23-844499D6A8D1">OnQuerySupportedCommandsComplete</a> method of the <a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/5C587408-DF03-4123-BA5A-C2CCC378F60A">IMbnDeviceService</a>
 

 

