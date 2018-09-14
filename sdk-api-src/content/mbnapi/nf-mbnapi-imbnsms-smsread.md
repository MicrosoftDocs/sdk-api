---
UID: NF:mbnapi.IMbnSms.SmsRead
title: IMbnSms::SmsRead
author: windows-sdk-content
description: Reads a set of SMS messages from a device.
old-location: mbn\imbnsms_smsread.htm
tech.root: mbn
ms.assetid: d15eab89-c2bb-45af-8a6b-077517973fb1
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IMbnSms interface [Microsoft Broadband Networks],SmsRead method, IMbnSms.SmsRead, IMbnSms::SmsRead, SmsRead, SmsRead method [Microsoft Broadband Networks], SmsRead method [Microsoft Broadband Networks],IMbnSms interface, mbn.imbnsms_smsread, mbnapi/IMbnSms::SmsRead
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
 - IMbnSms.SmsRead
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnSms::SmsRead


## -description


Reads a set of SMS messages from a device.


## -parameters




### -param smsFilter [in]

A pointer to a <a href="https://msdn.microsoft.com/f8dffd7b-3c12-43da-b61c-3c9aa8f1136f">MBN_SMS_FILTER</a> structure that defines the set of messages to read.


### -param smsFormat [in]

An <a href="https://msdn.microsoft.com/ece079e2-43a2-4ca9-9aa7-1b9484f0176e">MBN_SMS_FORMAT</a> value that specifies the format in which an SMS message should be read.  

For GSM devices, it should always be <b>MBN_SMS_FORMAT_PDU</b>.

For CDMA devices, if this is   specified as MBN_SMS_FORMAT_PDU, then the device will read a binary mode CDMA message. If it is specified as MBN_SMS_FORMAT_TEXT, then the device will read a text mode CDMA message. If the device doesn’t support the specified format then it can return an error code.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>smsFormat</i> or <i>smsFilter</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



Using <i>smsFilter</i>, an application can specify basic filters such as new messages, draft messages, or a specific message using an index.  A complex filter can be used by integrating a combination of basic filters. All the interfaces support the index based filters and new message type filters.  Support for other filters is optional for some interfaces. If the specified filter is not supported then operation completion callback function will return a status of <b>E_MBN_STATUS_FILTER_NOT_SUPPORTED</b>.

This is an asynchronous operation that will return immediately. If the method returns without error,  then the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/58478c9d-6df2-466b-85bc-1c571f4429ce">OnSmsReadComplete</a> method of the  <a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a>
 

 

