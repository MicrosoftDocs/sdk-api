---
UID: NF:mbnapi.IMbnSms.SmsSendCdma
title: IMbnSms::SmsSendCdma (mbnapi.h)
author: windows-sdk-content
description: Sends a message in CDMA format.
old-location: mbn\imbnsms_smssendcdma.htm
tech.root: mbn
ms.assetid: 5a370e00-929f-4ff9-861f-d0edc880f51d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnSms interface [Microsoft Broadband Networks],SmsSendCdma method, IMbnSms.SmsSendCdma, IMbnSms::SmsSendCdma, SmsSendCdma, SmsSendCdma method [Microsoft Broadband Networks], SmsSendCdma method [Microsoft Broadband Networks],IMbnSms interface, mbn.imbnsms_smssendcdma, mbnapi/IMbnSms::SmsSendCdma
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
 - IMbnSms.SmsSendCdma
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnSms::SmsSendCdma


## -description


Sends a message in CDMA format.


## -parameters




### -param address [in]

A null terminated string that contains the receiver's phone number.  The maximum size of the string is 15 digits.


### -param encoding [in]

A <a href="https://msdn.microsoft.com/c556d615-de98-4d05-86e4-88df84e98258">MBN_SMS_CDMA_ENCODING</a> value that specifies the data encoding.


### -param language [in]

An <a href="https://msdn.microsoft.com/569d5e28-d741-429e-a020-6724138272ae">MBN_SMS_CDMA_LANG</a> value that specifies the language.


### -param sizeInCharacters [in]

The number of encoded characters in the message. This can be different from the size of the message array.


### -param message [in]

An array of bytes containing the encoded CDMA message.  

The maximum size of this array is the <a href="https://msdn.microsoft.com/2aac8cad-565e-45e4-a7a4-88ebfab420ea">CdmaShortMsgSize</a> property of <a href="https://msdn.microsoft.com/ee261c32-aa17-496a-a568-d9da43e1e23a">IMbnSmsConfiguration</a>, however this can be no larger than <b>MBN_CDMA_SHORT_MSG_SIZE_MAX</b> (160).


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The device does not support sending SMS messages in the requested format.  For example, if this function is called for a GSM device.

</td>
</tr>
</table>
 




## -remarks



This method can be used to send a SMS message for a CDMA device. However, this is only when the CDMA device supports sending SMS. A calling application can learn if the device supports  this format by calling the <a href="https://msdn.microsoft.com/cfe8f638-ad17-4118-9c79-b7ebc81c726a">GetInterfaceCapability</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>.  It can then look for <b>MBN_SMS_CAPS_TEXT_SEND</b> in the <b>smsCaps</b> member of <a href="https://msdn.microsoft.com/faee7f53-b465-4240-b163-ce88fae764df">MBN_INTERFACE_CAPS</a>.


The <i>address</i> parameter can be in either of these formats.

<ul>
<li>"+ &lt;International Country Code&gt; &lt;SMS Service Center Number&gt;\0"</li>
<li>"&lt;SMS Service Center Number&gt;\0"</li>
</ul>


This is an asynchronous operation that will return immediately. If the method returns without error,  then the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/4c08b173-7e9e-4b4f-8068-1a90c57eea90">OnSmsSendComplete</a> method of the  <a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a>
 

 

