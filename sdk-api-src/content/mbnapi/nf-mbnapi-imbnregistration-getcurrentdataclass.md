---
UID: NF:mbnapi.IMbnRegistration.GetCurrentDataClass
title: IMbnRegistration::GetCurrentDataClass (mbnapi.h)
description: Gets the current data class in the current network.
helpviewer_keywords: ["GetCurrentDataClass","GetCurrentDataClass method [Microsoft Broadband Networks]","GetCurrentDataClass method [Microsoft Broadband Networks]","IMbnRegistration interface","IMbnRegistration interface [Microsoft Broadband Networks]","GetCurrentDataClass method","IMbnRegistration.GetCurrentDataClass","IMbnRegistration::GetCurrentDataClass","mbn.imbnregistration_getcurrentdataclass","mbnapi/IMbnRegistration::GetCurrentDataClass"]
old-location: mbn\imbnregistration_getcurrentdataclass.htm
tech.root: mbn
ms.assetid: 365458a4-74df-4283-94db-3d855acadffe
ms.date: 12/05/2018
ms.keywords: GetCurrentDataClass, GetCurrentDataClass method [Microsoft Broadband Networks], GetCurrentDataClass method [Microsoft Broadband Networks],IMbnRegistration interface, IMbnRegistration interface [Microsoft Broadband Networks],GetCurrentDataClass method, IMbnRegistration.GetCurrentDataClass, IMbnRegistration::GetCurrentDataClass, mbn.imbnregistration_getcurrentdataclass, mbnapi/IMbnRegistration::GetCurrentDataClass
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
 - IMbnRegistration::GetCurrentDataClass
 - mbnapi/IMbnRegistration::GetCurrentDataClass
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
 - IMbnRegistration.GetCurrentDataClass
---

# IMbnRegistration::GetCurrentDataClass


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the current data class in the current network.

## -parameters

### -param currentDataClass [out]

A pointer to a  <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_data_class">MBN_DATA_CLASS</a> value.  This parameter is meaningful only if the function returns <b>S_OK</b>.

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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The data classes are not available.  the Mobile Broadband service is currently probing the device for the information.  When the data classes are available, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onpacketservicestatechange">OnPacketServiceStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get the data classes.

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

The <b>GetCurrentDataClass</b> method returns the data class in the current network. This value can be set to <b>MBN_DATA_CLASS_NONE</b> if value is not known.

The current data class can change automatically as a device moves from one cellular network to another. Whenever such a change occurs, the Mobile Broadband service will notify applications by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onpacketservicestatechange">OnPacketServiceStateChange</a> method of  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

For the recoverable error <b>E_MBN_PIN_REQUIRED</b>, the Mobile Broadband service will again try to fetch this information from the device when the error condition is over (when a PIN is entered). Afterwards, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onpacketservicestatechange">OnPacketServiceStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a>