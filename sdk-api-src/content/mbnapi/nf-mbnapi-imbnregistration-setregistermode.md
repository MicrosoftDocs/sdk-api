---
UID: NF:mbnapi.IMbnRegistration.SetRegisterMode
title: IMbnRegistration::SetRegisterMode (mbnapi.h)
description: Sets the registration mode for the device.
helpviewer_keywords: ["IMbnRegistration interface [Microsoft Broadband Networks]","SetRegisterMode method","IMbnRegistration.SetRegisterMode","IMbnRegistration::SetRegisterMode","SetRegisterMode","SetRegisterMode method [Microsoft Broadband Networks]","SetRegisterMode method [Microsoft Broadband Networks]","IMbnRegistration interface","mbn.imbnregistration_setregistermode","mbnapi/IMbnRegistration::SetRegisterMode"]
old-location: mbn\imbnregistration_setregistermode.htm
tech.root: mbn
ms.assetid: 71434e46-7055-4721-8cc9-140e196b6097
ms.date: 12/05/2018
ms.keywords: IMbnRegistration interface [Microsoft Broadband Networks],SetRegisterMode method, IMbnRegistration.SetRegisterMode, IMbnRegistration::SetRegisterMode, SetRegisterMode, SetRegisterMode method [Microsoft Broadband Networks], SetRegisterMode method [Microsoft Broadband Networks],IMbnRegistration interface, mbn.imbnregistration_setregistermode, mbnapi/IMbnRegistration::SetRegisterMode
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
 - IMbnRegistration::SetRegisterMode
 - mbnapi/IMbnRegistration::SetRegisterMode
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
 - IMbnRegistration.SetRegisterMode
---

# IMbnRegistration::SetRegisterMode


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Sets the registration mode for the device.

## -parameters

### -param registerMode [in]

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_register_mode">MBN_REGISTER_MODE</a> value that specifies the new registration mode.

### -param providerID [in]

A string that specifies the provider ID of the network provider to which to register.  Must be <b>NULL</b> when <i>registerMode</i> is <b>MBN_REGISTER_MODE_AUTOMATIC</b>.

### -param dataClass [in]

A bitwise combination of OR <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_data_class">MBN_DATA_CLASS</a> values that specify the preferred data access technologies for the connection.  The Mobile Broadband service will register the highest available data class technology from this list.  If no data class from this list can be registered to, then the Mobile Broadband service will register to the best available data class.

### -param requestID [out]

A request ID set by the Mobile Broadband service to identify this asynchronous request.

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
The interface is invalid, most likely because the Mobile Broadband device has been removed from the system.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
There is already an active network connection. The registration mode cannot be changed while there is an already established data connection. The calling application should first disconnect the connection and then try changing registration mode. If the device is already in the requested mode and connected to the requested provider, then the return code will be <b>S_OK</b>.

</td>
</tr>
</table>

## -remarks

The <b>SetRegisterMode</b> method can be used to set a device into automatic or manual network selection mode. For manual registration mode the network ID to which the device should register is supplied in <i>providerID</i>.

Support for manual registration mode is optional and the application should verify that the device supports manual registration by checking for <b>MBN_CTRL_CAPS_REG_MANUAL</b> in the <i>interfaceCaps</i> parameter filled by the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getinterfacecapability">GetInterfaceCapability</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>. If an application sets the manual registration mode and it is not supported by the device, then this call will return <b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b>.


<b>SetRegisterMode</b> is asynchronous and will return immediately. If there is no error, on completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onsetregistermodecomplete">OnSetRegisterModeComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a>