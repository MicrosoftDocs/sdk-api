---
UID: NF:mbnapi.IMbnSms.SetSmsConfiguration
title: IMbnSms::SetSmsConfiguration (mbnapi.h)
description: Updates the SMS configuration for a device.
helpviewer_keywords: ["IMbnSms interface [Microsoft Broadband Networks]","SetSmsConfiguration method","IMbnSms.SetSmsConfiguration","IMbnSms::SetSmsConfiguration","SetSmsConfiguration","SetSmsConfiguration method [Microsoft Broadband Networks]","SetSmsConfiguration method [Microsoft Broadband Networks]","IMbnSms interface","mbn.imbnsms_setsmsconfiguration","mbnapi/IMbnSms::SetSmsConfiguration"]
old-location: mbn\imbnsms_setsmsconfiguration.htm
tech.root: mbn
ms.assetid: 8ed3af39-345b-4bfb-aea1-072a64f7921a
ms.date: 12/05/2018
ms.keywords: IMbnSms interface [Microsoft Broadband Networks],SetSmsConfiguration method, IMbnSms.SetSmsConfiguration, IMbnSms::SetSmsConfiguration, SetSmsConfiguration, SetSmsConfiguration method [Microsoft Broadband Networks], SetSmsConfiguration method [Microsoft Broadband Networks],IMbnSms interface, mbn.imbnsms_setsmsconfiguration, mbnapi/IMbnSms::SetSmsConfiguration
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
 - IMbnSms::SetSmsConfiguration
 - mbnapi/IMbnSms::SetSmsConfiguration
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
 - IMbnSms.SetSmsConfiguration
---

# IMbnSms::SetSmsConfiguration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Updates the SMS configuration for a device.

## -parameters

### -param smsConfiguration [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsconfiguration">IMbnSmsConfiguration</a> interface representing the new SMS configuration to update the device with.

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
The Mobile Broadband service is not running on the system.

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

An application can use <b>SetSmsConfiguration</b> to modify the default SMS Service Center address in the device.  

An application should perform following steps for setting SMS configuration of the device.


<ol>
<li>Get an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsconfiguration">IMbnSmsConfiguration</a>  interface by calling <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsms-getsmsconfiguration">GetSmsConfiguration</a>.</li>
<li>Modify the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsconfiguration">IMbnSmsConfiguration</a> interface obtained from step 1 with the new values that reflect the desired changes to the configuration..</li>
<li>Pass the modified <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsconfiguration">IMbnSmsConfiguration</a>  to <b>SetSmsConfiguration</b>.</li>
</ol>
This is an asynchronous operation that will return immediately. If the method returns without error,  then the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsetsmsconfigurationcomplete">OnSetSmsConfigurationComplete</a> method of the  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a>



<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsconfiguration">IMbnSmsConfiguration</a>