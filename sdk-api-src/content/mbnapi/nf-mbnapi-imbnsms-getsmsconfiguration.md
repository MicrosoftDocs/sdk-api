---
UID: NF:mbnapi.IMbnSms.GetSmsConfiguration
title: IMbnSms::GetSmsConfiguration (mbnapi.h)
description: Gets the SMS configuration of a device.
helpviewer_keywords: ["GetSmsConfiguration","GetSmsConfiguration method [Microsoft Broadband Networks]","GetSmsConfiguration method [Microsoft Broadband Networks]","IMbnSms interface","IMbnSms interface [Microsoft Broadband Networks]","GetSmsConfiguration method","IMbnSms.GetSmsConfiguration","IMbnSms::GetSmsConfiguration","mbn.imbnsms_getsmsconfiguration","mbnapi/IMbnSms::GetSmsConfiguration"]
old-location: mbn\imbnsms_getsmsconfiguration.htm
tech.root: mbn
ms.assetid: b868bb6f-3ac0-4d77-82dd-b9bc94882a8b
ms.date: 12/05/2018
ms.keywords: GetSmsConfiguration, GetSmsConfiguration method [Microsoft Broadband Networks], GetSmsConfiguration method [Microsoft Broadband Networks],IMbnSms interface, IMbnSms interface [Microsoft Broadband Networks],GetSmsConfiguration method, IMbnSms.GetSmsConfiguration, IMbnSms::GetSmsConfiguration, mbn.imbnsms_getsmsconfiguration, mbnapi/IMbnSms::GetSmsConfiguration
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
 - IMbnSms::GetSmsConfiguration
 - mbnapi/IMbnSms::GetSmsConfiguration
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
 - IMbnSms.GetSmsConfiguration
---

# IMbnSms::GetSmsConfiguration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the SMS configuration of a device.

## -parameters

### -param smsConfiguration [out, retval]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsconfiguration">IMbnSmsConfiguration</a> interface representing the SMS configuration of the device.

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
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The SMS configuration is not available.  The Mobile Broadband service is probing the device for the information.  The calling application can be notified when the SMS configuration is available by registering for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsconfigurationchange">OnSmsConfigurationChange</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a> interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get this information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
There is no SIM in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
There is a  bad SIM in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
SMS is not supported by the device.

</td>
</tr>
</table>

## -remarks

For recoverable errors such as <b>E_MBN_PIN_REQUIRED</b>, <b>E_MBN_SIM_NOT_INSERTED</b>, and <b>E_MBN_BAD_SIM</b>, the Mobile Broadband service will query the device again for this information when error condition is over. For example, if the device required a PIN to be entered to retrieve this information then it will return <b>E_MBN_PIN_REQUIRED</b>. When an application enters the PIN to unlock the device then the Mobile Broadband service will again try to get this information from the device. The Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsconfigurationchange">OnSmsConfigurationChange</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a> interface

SMS configuration can be updated by the network or device without any change request by any application. In such a  case,  the Mobile Broadband service will notify all the registered applications by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsconfigurationchange">OnSmsConfigurationChange</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a>