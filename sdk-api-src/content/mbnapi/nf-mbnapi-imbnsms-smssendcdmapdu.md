---
UID: NF:mbnapi.IMbnSms.SmsSendCdmaPdu
title: IMbnSms::SmsSendCdmaPdu
author: windows-sdk-content
description: Sends a message in CDMA binary format.
old-location: mbn\imbnsms_smssendcdmapdu.htm
old-project: mbn
ms.assetid: 8bc0cad6-dee3-4325-b5e9-397bbd346a87
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnSms interface [Microsoft Broadband Networks],SmsSendCdmaPdu method, IMbnSms.SmsSendCdmaPdu, IMbnSms::SmsSendCdmaPdu, SmsSendCdmaPdu, SmsSendCdmaPdu method [Microsoft Broadband Networks], SmsSendCdmaPdu method [Microsoft Broadband Networks],IMbnSms interface, mbn.imbnsms_smssendcdmapdu, mbnapi/IMbnSms::SmsSendCdmaPdu
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
 - IMbnSms.SmsSendCdmaPdu
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSms::SmsSendCdmaPdu


## -description


Sends a message in CDMA binary format.


## -parameters




### -param message [in]

Byte array representing the encoded CMDA message as per section 3.4.2.1 "SMS Point-to-Point Message” in 3GPP2 specification C.S0015-A “Short Message Service (SMS) for Wideband Spread Spectrum Systems”. SMS will only support the Wireless Messaging Teleservice (WMT) format.  


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
<i>message</i> is invalid.

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



This method is applicable only to CDMA devices.

<b>SmsSendCdmaPdu</b> can be used to send a SMS message in binary format encoded as per section 3.4.2.1 of "SMS Point-to-Point Message” in 3GPP2 specification C.S0015-A “Short Message Service (SMS) for Wideband Spread Spectrum Systems”. SMS will only support Wireless Messaging Teleservice (WMT) format. 


<b>SmsSendCdmaPdu</b> should be called only when the CDMA device supports sending SMS in binary format. The device reports this format by setting <b>MBN_SMS_PDU_SEND</b> in <a href="https://msdn.microsoft.com/faee7f53-b465-4240-b163-ce88fae764df">MBN_INTERFACE_CAPS</a>.


This is an asynchronous operation and method call will return immediately. If method returns without any error then operation will be performed asynchronously. Windows will notify applications about completion status of operation by calling the <a href="https://msdn.microsoft.com/4c08b173-7e9e-4b4f-8068-1a90c57eea90">OnSmsSendComplete</a> method of <a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a>.





## -see-also




<a href="https://msdn.microsoft.com/4a5fae5a-91d5-4a94-ac54-cb641147e8dc">IMbnSms</a>
 

 

