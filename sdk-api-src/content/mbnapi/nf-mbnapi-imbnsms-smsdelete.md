---
UID: NF:mbnapi.IMbnSms.SmsDelete
title: IMbnSms::SmsDelete
author: windows-sdk-content
description: Deletes a set of SMS messages from a device.
old-location: mbn\imbnsms_smsdelete.htm
tech.root: mbn
ms.assetid: cd37582e-891d-4f6a-aba3-01ad3101a6b9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMbnSms interface [Microsoft Broadband Networks],SmsDelete method, IMbnSms.SmsDelete, IMbnSms::SmsDelete, SmsDelete, SmsDelete method [Microsoft Broadband Networks], SmsDelete method [Microsoft Broadband Networks],IMbnSms interface, mbn.imbnsms_smsdelete, mbnapi/IMbnSms::SmsDelete
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMbnSms.SmsDelete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mbnapi.h
: 
- IMbnSms.SmsDelete
: 
---

# IMbnSms::SmsDelete


## -description


Deletes a set of SMS messages from a device.


## -parameters




### -param smsFilter [in]

A pointer to a <a href="https://msdn.microsoft.com/f8dffd7b-3c12-43da-b61c-3c9aa8f1136f">MBN_SMS_FILTER</a> structure that defines the set of messages to delete.


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
The Mobile Broadband service is not running on this system.

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



This is an asynchronous operation that will return immediately. If the method returns without error,  then the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/bac1c7b3-fedc-47fb-822c-712805a86f6e">OnSmsDeleteComplete</a> method of the  <a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a>
 

 

