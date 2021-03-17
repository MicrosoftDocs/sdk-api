---
UID: NF:mbnapi.IMbnRegistration.GetRoamingText
title: IMbnRegistration::GetRoamingText (mbnapi.h)
description: Gets the roaming text describing the roaming provider.
helpviewer_keywords: ["GetRoamingText","GetRoamingText method [Microsoft Broadband Networks]","GetRoamingText method [Microsoft Broadband Networks]","IMbnRegistration interface","IMbnRegistration interface [Microsoft Broadband Networks]","GetRoamingText method","IMbnRegistration.GetRoamingText","IMbnRegistration::GetRoamingText","mbn.imbnregistration_getroamingtext","mbnapi/IMbnRegistration::GetRoamingText"]
old-location: mbn\imbnregistration_getroamingtext.htm
tech.root: mbn
ms.assetid: a2911387-7497-43c5-bc1c-db093f31186c
ms.date: 12/05/2018
ms.keywords: GetRoamingText, GetRoamingText method [Microsoft Broadband Networks], GetRoamingText method [Microsoft Broadband Networks],IMbnRegistration interface, IMbnRegistration interface [Microsoft Broadband Networks],GetRoamingText method, IMbnRegistration.GetRoamingText, IMbnRegistration::GetRoamingText, mbn.imbnregistration_getroamingtext, mbnapi/IMbnRegistration::GetRoamingText
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
 - IMbnRegistration::GetRoamingText
 - mbnapi/IMbnRegistration::GetRoamingText
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
 - IMbnRegistration.GetRoamingText
---

# IMbnRegistration::GetRoamingText


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the roaming text describing the roaming provider.

## -parameters

### -param roamingText [out]

Pointer to a string that contains additional information about a network with which the device is roaming. The maximum length is <b>MBN_ROAMTEXT_LEN</b> characters.  The string is filled only when the method returns <b>S_OK</b> for success.  Upon success, the calling application must free the allocated memory by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

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
The roaming text is not available.  The Mobile Broadband service is currently probing the device for the information.  When the roaming text is available, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onregistermodeavailable">OnRegisterModeAvailable</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get the roaming text.

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

The <b>GetRoamingText</b> method can get a text string containing additional information about the network when the registration state is either <b>MBN_REGISTER_STATE_PARTNER</b> or <b>MBN_REGISTER_STATE_ROAMING</b>.

This information may change when the Mobile Broadband device moves from one network to another. This includes whenever there is a change from <b>MBN_REGISTER_STATE_HOME</b> to <b>MBN_REGISTER_STATE_SEARCHING</b> in the network registration state.  This also occurs  when there is a change in the registered network, such as when a network moves its registration from one provider to another.  After such changes, the Mobile Broadband service will call the  <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onregisterstatechange">OnRegisterStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

For the recoverable error <b>E_MBN_PIN_REQUIRED</b>, the Mobile Broadband service will again try to fetch this information from the device when the error condition is over (when a PIN is entered).  Then it will call the  <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onregisterstatechange">OnRegisterStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a>