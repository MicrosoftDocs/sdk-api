---
UID: NF:mbnapi.IMbnSms.GetSmsStatus
title: IMbnSms::GetSmsStatus (mbnapi.h)
description: Gets the SMS status for a device.
helpviewer_keywords: ["GetSmsStatus","GetSmsStatus method [Microsoft Broadband Networks]","GetSmsStatus method [Microsoft Broadband Networks]","IMbnSms interface","IMbnSms interface [Microsoft Broadband Networks]","GetSmsStatus method","IMbnSms.GetSmsStatus","IMbnSms::GetSmsStatus","mbn.imbnsms_getsmsstatus","mbnapi/IMbnSms::GetSmsStatus"]
old-location: mbn\imbnsms_getsmsstatus.htm
tech.root: mbn
ms.assetid: 58cb60dd-160c-4e1c-a244-7f20b5e79b64
ms.date: 12/05/2018
ms.keywords: GetSmsStatus, GetSmsStatus method [Microsoft Broadband Networks], GetSmsStatus method [Microsoft Broadband Networks],IMbnSms interface, IMbnSms interface [Microsoft Broadband Networks],GetSmsStatus method, IMbnSms.GetSmsStatus, IMbnSms::GetSmsStatus, mbn.imbnsms_getsmsstatus, mbnapi/IMbnSms::GetSmsStatus
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
 - IMbnSms::GetSmsStatus
 - mbnapi/IMbnSms::GetSmsStatus
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
 - IMbnSms.GetSmsStatus
---

# IMbnSms::GetSmsStatus


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the SMS status for a device.

## -parameters

### -param smsStatusInfo [out]

A pointer to a <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_sms_status_info">MBN_SMS_STATUS_INFO</a> structure, containing the status information for the device.

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
The SMS status is not available.  The Mobile Broadband service is probing the device for the information.  The calling application can be notified when the SMS status is available by registering for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsstatuschange">OnSmsStatusChange</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a> interface.

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
A SIM is not inserted in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
A bad SIM is inserted in the device.

</td>
</tr>
</table>

## -remarks

For recoverable errors such as <b>E_MBN_PIN_REQUIRED</b>, <b>E_MBN_SIM_NOT_INSERTED</b>, and <b>E_MBN_BAD_SIM</b>, the Mobile Broadband service will query the device again for this information when error condition is over. For example, if the device required a PIN to be entered to retrieve this information then it will return <b>E_MBN_PIN_REQUIRED</b>. When an application enters the PIN to unlock the device then the Mobile Broadband service will again try to get this information from the device. The Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsstatuschange">OnSmsStatusChange</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a> interface

The SMS Message store status can change because of new message received by the system. On any change in the message store status, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsstatuschange">OnSmsStatusChange</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvent</a> interface.


Application issued operations such as the  reading or deleting of messages may reset <b>flag</b> in <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_sms_status_info">MBN_SMS_STATUS_INFO</a> structure. A change in the SMS store caused by this reset will not result in the calling of any notification method.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a>