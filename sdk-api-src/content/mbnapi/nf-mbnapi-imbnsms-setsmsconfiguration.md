---
UID: NF:mbnapi.IMbnSms.SetSmsConfiguration
title: IMbnSms::SetSmsConfiguration
author: windows-sdk-content
description: Updates the SMS configuration for a device.
old-location: mbn\imbnsms_setsmsconfiguration.htm
old-project: mbn
ms.assetid: 8ed3af39-345b-4bfb-aea1-072a64f7921a
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IMbnSms interface [Microsoft Broadband Networks],SetSmsConfiguration method, IMbnSms.SetSmsConfiguration, IMbnSms::SetSmsConfiguration, SetSmsConfiguration, SetSmsConfiguration method [Microsoft Broadband Networks], SetSmsConfiguration method [Microsoft Broadband Networks],IMbnSms interface, mbn.imbnsms_setsmsconfiguration, mbnapi/IMbnSms::SetSmsConfiguration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IMbnSms.SetSmsConfiguration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSms::SetSmsConfiguration


## -description


Updates the SMS configuration for a device.


## -parameters




### -param smsConfiguration [in]

An <a href="https://msdn.microsoft.com/ee261c32-aa17-496a-a568-d9da43e1e23a">IMbnSmsConfiguration</a> interface representing the new SMS configuration to update the device with.


### -param requestID [out]

A pointer to a request ID issued by the Mobile Broadband service to identify this request.


## -returns



This method can return one of these values.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The interface is invalid, most likely because the device was removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The interface is invalid. Most likely the Mobile Broadband device has been removed from the system.

</td>
</tr>
</table>
 




## -remarks



An application can use <b>SetSmsConfiguration</b> to modify the default SMS Service Center address in the device.  

An application should perform following steps for setting SMS configuration of the device.


<ol>
<li>Get an <a href="https://msdn.microsoft.com/ee261c32-aa17-496a-a568-d9da43e1e23a">IMbnSmsConfiguration</a>  interface by calling <a href="https://msdn.microsoft.com/b868bb6f-3ac0-4d77-82dd-b9bc94882a8b">GetSmsConfiguration</a>.</li>
<li>Modify the <a href="https://msdn.microsoft.com/ee261c32-aa17-496a-a568-d9da43e1e23a">IMbnSmsConfiguration</a> interface obtained from step 1 with the new values that reflect the desired changes to the configuration..</li>
<li>Pass the modified <a href="https://msdn.microsoft.com/ee261c32-aa17-496a-a568-d9da43e1e23a">IMbnSmsConfiguration</a>  to <b>SetSmsConfiguration</b>.</li>
</ol>
This is an asynchronous operation that will return immediately. If the method returns without error,  then the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/d5e5b1fc-88c3-4438-a160-f9969ed6d91a">OnSetSmsConfigurationComplete</a> method of the  <a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a> interface. 




## -see-also




<a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a>



<a href="https://msdn.microsoft.com/ee261c32-aa17-496a-a568-d9da43e1e23a">IMbnSmsConfiguration</a>
 

 

