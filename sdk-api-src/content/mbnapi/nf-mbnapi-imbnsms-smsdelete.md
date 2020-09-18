---
UID: NF:mbnapi.IMbnSms.SmsDelete
title: IMbnSms::SmsDelete (mbnapi.h)
description: Deletes a set of SMS messages from a device.
helpviewer_keywords: ["IMbnSms interface [Microsoft Broadband Networks]","SmsDelete method","IMbnSms.SmsDelete","IMbnSms::SmsDelete","SmsDelete","SmsDelete method [Microsoft Broadband Networks]","SmsDelete method [Microsoft Broadband Networks]","IMbnSms interface","mbn.imbnsms_smsdelete","mbnapi/IMbnSms::SmsDelete"]
old-location: mbn\imbnsms_smsdelete.htm
tech.root: mbn
ms.assetid: cd37582e-891d-4f6a-aba3-01ad3101a6b9
ms.date: 12/05/2018
ms.keywords: IMbnSms interface [Microsoft Broadband Networks],SmsDelete method, IMbnSms.SmsDelete, IMbnSms::SmsDelete, SmsDelete, SmsDelete method [Microsoft Broadband Networks], SmsDelete method [Microsoft Broadband Networks],IMbnSms interface, mbn.imbnsms_smsdelete, mbnapi/IMbnSms::SmsDelete
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
 - IMbnSms::SmsDelete
 - mbnapi/IMbnSms::SmsDelete
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
 - IMbnSms.SmsDelete
---

# IMbnSms::SmsDelete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Deletes a set of SMS messages from a device.

## -parameters

### -param smsFilter [in]

A pointer to a <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_sms_filter">MBN_SMS_FILTER</a> structure that defines the set of messages to delete.

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

This is an asynchronous operation that will return immediately. If the method returns without error,  then the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsdeletecomplete">OnSmsDeleteComplete</a> method of the  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a>