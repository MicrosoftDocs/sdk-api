---
UID: NF:mbnapi.IMbnSms.SmsSendCdmaPdu
title: IMbnSms::SmsSendCdmaPdu (mbnapi.h)
description: Sends a message in CDMA binary format.
helpviewer_keywords: ["IMbnSms interface [Microsoft Broadband Networks]","SmsSendCdmaPdu method","IMbnSms.SmsSendCdmaPdu","IMbnSms::SmsSendCdmaPdu","SmsSendCdmaPdu","SmsSendCdmaPdu method [Microsoft Broadband Networks]","SmsSendCdmaPdu method [Microsoft Broadband Networks]","IMbnSms interface","mbn.imbnsms_smssendcdmapdu","mbnapi/IMbnSms::SmsSendCdmaPdu"]
old-location: mbn\imbnsms_smssendcdmapdu.htm
tech.root: mbn
ms.assetid: 8bc0cad6-dee3-4325-b5e9-397bbd346a87
ms.date: 12/05/2018
ms.keywords: IMbnSms interface [Microsoft Broadband Networks],SmsSendCdmaPdu method, IMbnSms.SmsSendCdmaPdu, IMbnSms::SmsSendCdmaPdu, SmsSendCdmaPdu, SmsSendCdmaPdu method [Microsoft Broadband Networks], SmsSendCdmaPdu method [Microsoft Broadband Networks],IMbnSms interface, mbn.imbnsms_smssendcdmapdu, mbnapi/IMbnSms::SmsSendCdmaPdu
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
 - IMbnSms::SmsSendCdmaPdu
 - mbnapi/IMbnSms::SmsSendCdmaPdu
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
 - IMbnSms.SmsSendCdmaPdu
---

# IMbnSms::SmsSendCdmaPdu


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

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


<b>SmsSendCdmaPdu</b> should be called only when the CDMA device supports sending SMS in binary format. The device reports this format by setting <b>MBN_SMS_PDU_SEND</b> in <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a>.


This is an asynchronous operation and method call will return immediately. If method returns without any error then operation will be performed asynchronously. Windows will notify applications about completion status of operation by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmssendcomplete">OnSmsSendComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a>