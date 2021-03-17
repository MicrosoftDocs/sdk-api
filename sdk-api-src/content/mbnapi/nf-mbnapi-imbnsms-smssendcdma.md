---
UID: NF:mbnapi.IMbnSms.SmsSendCdma
title: IMbnSms::SmsSendCdma (mbnapi.h)
description: Sends a message in CDMA format.
helpviewer_keywords: ["IMbnSms interface [Microsoft Broadband Networks]","SmsSendCdma method","IMbnSms.SmsSendCdma","IMbnSms::SmsSendCdma","SmsSendCdma","SmsSendCdma method [Microsoft Broadband Networks]","SmsSendCdma method [Microsoft Broadband Networks]","IMbnSms interface","mbn.imbnsms_smssendcdma","mbnapi/IMbnSms::SmsSendCdma"]
old-location: mbn\imbnsms_smssendcdma.htm
tech.root: mbn
ms.assetid: 5a370e00-929f-4ff9-861f-d0edc880f51d
ms.date: 12/05/2018
ms.keywords: IMbnSms interface [Microsoft Broadband Networks],SmsSendCdma method, IMbnSms.SmsSendCdma, IMbnSms::SmsSendCdma, SmsSendCdma, SmsSendCdma method [Microsoft Broadband Networks], SmsSendCdma method [Microsoft Broadband Networks],IMbnSms interface, mbn.imbnsms_smssendcdma, mbnapi/IMbnSms::SmsSendCdma
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnSms::SmsSendCdma
 - mbnapi/IMbnSms::SmsSendCdma
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnSms.SmsSendCdma
---

# IMbnSms::SmsSendCdma


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Sends a message in CDMA format.

## -parameters

### -param address [in]

A null terminated string that contains the receiver's phone number.  The maximum size of the string is 15 digits.

### -param encoding [in]

A <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_sms_cdma_encoding">MBN_SMS_CDMA_ENCODING</a> value that specifies the data encoding.

### -param language [in]

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_sms_cdma_lang">MBN_SMS_CDMA_LANG</a> value that specifies the language.

### -param sizeInCharacters [in]

The number of encoded characters in the message. This can be different from the size of the message array.

### -param message [in]

An array of bytes containing the encoded CDMA message.  

The maximum size of this array is the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsconfiguration-get_cdmashortmsgsize">CdmaShortMsgSize</a> property of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsconfiguration">IMbnSmsConfiguration</a>, however this can be no larger than <b>MBN_CDMA_SHORT_MSG_SIZE_MAX</b> (160).

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

This method can be used to send a SMS message for a CDMA device. However, this is only when the CDMA device supports sending SMS. A calling application can learn if the device supports  this format by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getinterfacecapability">GetInterfaceCapability</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.  It can then look for <b>MBN_SMS_CAPS_TEXT_SEND</b> in the <b>smsCaps</b> member of <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a>.


The <i>address</i> parameter can be in either of these formats.

<ul>
<li>"+ &lt;International Country Code&gt; &lt;SMS Service Center Number&gt;\0"</li>
<li>"&lt;SMS Service Center Number&gt;\0"</li>
</ul>


This is an asynchronous operation that will return immediately. If the method returns without error,  then the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmssendcomplete">OnSmsSendComplete</a> method of the  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a>