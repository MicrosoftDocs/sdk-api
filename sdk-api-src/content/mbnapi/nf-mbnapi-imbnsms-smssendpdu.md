---
UID: NF:mbnapi.IMbnSms.SmsSendPdu
title: IMbnSms::SmsSendPdu (mbnapi.h)
description: Sends a message in PDU format.
helpviewer_keywords: ["IMbnSms interface [Microsoft Broadband Networks]","SmsSendPdu method","IMbnSms.SmsSendPdu","IMbnSms::SmsSendPdu","SmsSendPdu","SmsSendPdu method [Microsoft Broadband Networks]","SmsSendPdu method [Microsoft Broadband Networks]","IMbnSms interface","mbn.imbnsms_smssendpdu","mbnapi/IMbnSms::SmsSendPdu"]
old-location: mbn\imbnsms_smssendpdu.htm
tech.root: mbn
ms.assetid: c8f5bde5-d28c-4799-9f46-7b02745e6bfb
ms.date: 12/05/2018
ms.keywords: IMbnSms interface [Microsoft Broadband Networks],SmsSendPdu method, IMbnSms.SmsSendPdu, IMbnSms::SmsSendPdu, SmsSendPdu, SmsSendPdu method [Microsoft Broadband Networks], SmsSendPdu method [Microsoft Broadband Networks],IMbnSms interface, mbn.imbnsms_smssendpdu, mbnapi/IMbnSms::SmsSendPdu
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
 - IMbnSms::SmsSendPdu
 - mbnapi/IMbnSms::SmsSendPdu
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
 - IMbnSms.SmsSendPdu
---

# IMbnSms::SmsSendPdu


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Sends a message in PDU format.

## -parameters

### -param pduData [in]

A string representing the PDU message in hexadecimal format.

### -param size [in]

The size of PDU message in number of bytes before converting to hexadecimal string format and excluding the service center address length.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pduData</i> or <i>size</i> are invalid.

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
The device does not support sending SMS messages in the requested format.  For example, if this function is called for a CDMA device.

</td>
</tr>
</table>

## -remarks

  This data in <i>pduData</i> is compliant to the PDU structure defined in 3GPP TS 27.005 and 3GPP TS 23.040.

The table below shows an example of how a PDU message containing the message "Hello" would be structured.


<table>
<tr>
<th>Example</th>
<td>07</td>
<td>91198994000010</td>
<td>11000A9189945086180000AA05C8329BFD06</td>
</tr>
<tr>
<th>Contents</th>
<td>Size of Service Center Address</td>
<td>Service Center Address</td>
<td>PDU in hexadecimal format</td>
</tr>
<tr>
<th>Size</th>
<td>1 byte</td>
<td>Variable</td>
<td>Variable</td>
</tr>
</table>
 



This function should be called only for GSM devices that support sending SMS in PDU format. A device reports this ability by setting <b>MBN_SMS_CAPS_PDU_SEND</b> in <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a>.

This is an asynchronous operation that will return immediately. If the method returns without error,  then the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmssendcomplete">OnSmsSendComplete</a> method of the  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a>