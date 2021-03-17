---
UID: NF:mbnapi.IMbnRegistrationEvents.OnRegisterStateChange
title: IMbnRegistrationEvents::OnRegisterStateChange (mbnapi.h)
description: Notification method called by the Mobile Broadband service to indicate a change in the device's registration state.
helpviewer_keywords: ["IMbnRegistrationEvents interface [Microsoft Broadband Networks]","OnRegisterStateChange method","IMbnRegistrationEvents.OnRegisterStateChange","IMbnRegistrationEvents::OnRegisterStateChange","OnRegisterStateChange","OnRegisterStateChange method [Microsoft Broadband Networks]","OnRegisterStateChange method [Microsoft Broadband Networks]","IMbnRegistrationEvents interface","mbn.imbnregistrationevents_onregisterstatechange","mbnapi/IMbnRegistrationEvents::OnRegisterStateChange"]
old-location: mbn\imbnregistrationevents_onregisterstatechange.htm
tech.root: mbn
ms.assetid: 62393a9b-70e5-4819-8df1-59b94c1b6922
ms.date: 12/05/2018
ms.keywords: IMbnRegistrationEvents interface [Microsoft Broadband Networks],OnRegisterStateChange method, IMbnRegistrationEvents.OnRegisterStateChange, IMbnRegistrationEvents::OnRegisterStateChange, OnRegisterStateChange, OnRegisterStateChange method [Microsoft Broadband Networks], OnRegisterStateChange method [Microsoft Broadband Networks],IMbnRegistrationEvents interface, mbn.imbnregistrationevents_onregisterstatechange, mbnapi/IMbnRegistrationEvents::OnRegisterStateChange
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
 - IMbnRegistrationEvents::OnRegisterStateChange
 - mbnapi/IMbnRegistrationEvents::OnRegisterStateChange
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
 - IMbnRegistrationEvents.OnRegisterStateChange
---

# IMbnRegistrationEvents::OnRegisterStateChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method called by the Mobile Broadband service to indicate a change in the device's registration state.

## -parameters

### -param newInterface [in]

Pointer to an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a> interface that represents the applicable device.

## -returns

This method must return <b>S_OK</b>.

## -remarks

The <b>OnRegisterStateChange</b> method is called by the Mobile Broadband service to signal a change in the device registration state. It may  be called if any of the following changes:

<ul>
<li>There is a change in the registration state of the device.  For example, if the device goes from its home network to a roaming network, then the registration state can change from <b>MBN_REGISTER_STATE_HOME</b> to <b>MBN_REGISTER_STATE_ROAMING</b>.</li>
<li>There is a change in registered provider ID, name, or roaming text.</li>
<li>There is a change in the last reported network error code for a registration operation.</li>
</ul>
An application can use the passed <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a> interface to get the updated registration state data.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>