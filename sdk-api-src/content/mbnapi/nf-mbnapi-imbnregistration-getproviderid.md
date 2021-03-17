---
UID: NF:mbnapi.IMbnRegistration.GetProviderID
title: IMbnRegistration::GetProviderID (mbnapi.h)
description: Gets the provider ID for the currently registered network.
helpviewer_keywords: ["GetProviderID","GetProviderID method [Microsoft Broadband Networks]","GetProviderID method [Microsoft Broadband Networks]","IMbnRegistration interface","IMbnRegistration interface [Microsoft Broadband Networks]","GetProviderID method","IMbnRegistration.GetProviderID","IMbnRegistration::GetProviderID","mbn.imbnregistration_getproviderid","mbnapi/IMbnRegistration::GetProviderID"]
old-location: mbn\imbnregistration_getproviderid.htm
tech.root: mbn
ms.assetid: 0b21a103-2b49-4d99-8041-c9da9cbc5750
ms.date: 12/05/2018
ms.keywords: GetProviderID, GetProviderID method [Microsoft Broadband Networks], GetProviderID method [Microsoft Broadband Networks],IMbnRegistration interface, IMbnRegistration interface [Microsoft Broadband Networks],GetProviderID method, IMbnRegistration.GetProviderID, IMbnRegistration::GetProviderID, mbn.imbnregistration_getproviderid, mbnapi/IMbnRegistration::GetProviderID
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
 - IMbnRegistration::GetProviderID
 - mbnapi/IMbnRegistration::GetProviderID
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
 - IMbnRegistration.GetProviderID
---

# IMbnRegistration::GetProviderID


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the provider ID for the currently registered network.

## -parameters

### -param providerID [out]

Pointer to a string that contains the ID of the currently registered provider.  The maximum length is <b>MBN_PROVIDERID_LEN</b> characters.  The string is filled only when the method returns <b>S_OK</b> for success.  Upon success, the calling application must free the allocated memory by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

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
The provider ID is not available.  The Mobile Broadband service is currently probing the device for the information.  When the provider ID is available, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onregistermodeavailable">OnRegisterModeAvailable</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get the provider ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MBN_SIM_NOT_INSERTED</b></dt>
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

The <b>GetProviderID</b> method gets  the ID of the currently registered provider. For auto network selection mode this is the ID of the network to which the device is currently registered. If the network selection mode is manual then this field will contain the provider ID of the network to which device will try to register. For CDMA devices it is set to <b>MBN_CDMA_DEFAULT_PROVIDER_ID</b> if the provider ID is not known.

This information may change when the Mobile Broadband device moves from one network to another. This includes whenever there is a change from <b>MBN_REGISTER_STATE_HOME</b> to <b>MBN_REGISTER_STATE_SEARCHING</b> in the network registration state.  This also occurs  when there is a change in the registered network, such as when a network moves its registration from one provider to another.  After such changes, the Mobile Broadband service will call the  <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onregisterstatechange">OnRegisterStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>. When this happens, the application should call <b>GetProviderID</b>.

For the recoverable error <b>E_MBN_PIN_REQUIRED</b>, the Mobile Broadband service will again try to fetch this information from the device when the error condition is over (when a PIN is entered). Afterwards, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onpacketservicestatechange">OnPacketServiceStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a>