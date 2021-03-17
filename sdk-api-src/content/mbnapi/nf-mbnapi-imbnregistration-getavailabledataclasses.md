---
UID: NF:mbnapi.IMbnRegistration.GetAvailableDataClasses
title: IMbnRegistration::GetAvailableDataClasses (mbnapi.h)
description: Gets the available data classes in the current network.
helpviewer_keywords: ["GetAvailableDataClasses","GetAvailableDataClasses method [Microsoft Broadband Networks]","GetAvailableDataClasses method [Microsoft Broadband Networks]","IMbnRegistration interface","IMbnRegistration interface [Microsoft Broadband Networks]","GetAvailableDataClasses method","IMbnRegistration.GetAvailableDataClasses","IMbnRegistration::GetAvailableDataClasses","mbn.imbnregistration_getavailabledataclasses","mbnapi/IMbnRegistration::GetAvailableDataClasses"]
old-location: mbn\imbnregistration_getavailabledataclasses.htm
tech.root: mbn
ms.assetid: fb799232-0ef5-4fbd-9b7f-a106ef440a68
ms.date: 12/05/2018
ms.keywords: GetAvailableDataClasses, GetAvailableDataClasses method [Microsoft Broadband Networks], GetAvailableDataClasses method [Microsoft Broadband Networks],IMbnRegistration interface, IMbnRegistration interface [Microsoft Broadband Networks],GetAvailableDataClasses method, IMbnRegistration.GetAvailableDataClasses, IMbnRegistration::GetAvailableDataClasses, mbn.imbnregistration_getavailabledataclasses, mbnapi/IMbnRegistration::GetAvailableDataClasses
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
 - IMbnRegistration::GetAvailableDataClasses
 - mbnapi/IMbnRegistration::GetAvailableDataClasses
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
 - IMbnRegistration.GetAvailableDataClasses
---

# IMbnRegistration::GetAvailableDataClasses


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the available data classes in the current network.

## -parameters

### -param availableDataClasses [out]

A pointer to a bitwise OR combination of <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_data_class">MBN_DATA_CLASS</a> values.  This parameter is meaningful only if the function returns <b>S_OK</b>.

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
</table>

## -remarks

<b>GetAvailableDataClasses</b> returns the set of data class possible in the current network. These values can be set to <b>MBN_DATA_CLASS_NONE</b> if value is not known.

Available data classes can change automatically as a device moves from one cell to another. Whenever such a change occurs, the Mobile Broadband service will notify applications by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onpacketservicestatechange">OnPacketServiceStateChange</a> method of  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

For the recoverable error <b>E_MBN_PIN_REQUIRED</b>, the Mobile Broadband service will again try to fetch this information from the device when the error condition is over (when a PIN is entered). Afterwards, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onpacketservicestatechange">OnPacketServiceStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a>