---
UID: NF:mbnapi.IMbnRegistrationEvents.OnRegisterModeAvailable
title: IMbnRegistrationEvents::OnRegisterModeAvailable (mbnapi.h)
description: Notification method called by the Mobile Broadband service to indicate that registration mode information is available.
helpviewer_keywords: ["IMbnRegistrationEvents interface [Microsoft Broadband Networks]","OnRegisterModeAvailable method","IMbnRegistrationEvents.OnRegisterModeAvailable","IMbnRegistrationEvents::OnRegisterModeAvailable","OnRegisterModeAvailable","OnRegisterModeAvailable method [Microsoft Broadband Networks]","OnRegisterModeAvailable method [Microsoft Broadband Networks]","IMbnRegistrationEvents interface","mbn.imbnregistrationevents_onregistermodeavailable","mbnapi/IMbnRegistrationEvents::OnRegisterModeAvailable"]
old-location: mbn\imbnregistrationevents_onregistermodeavailable.htm
tech.root: mbn
ms.assetid: 5c916f16-e8f5-4c8a-942c-3a9ae11905a7
ms.date: 12/05/2018
ms.keywords: IMbnRegistrationEvents interface [Microsoft Broadband Networks],OnRegisterModeAvailable method, IMbnRegistrationEvents.OnRegisterModeAvailable, IMbnRegistrationEvents::OnRegisterModeAvailable, OnRegisterModeAvailable, OnRegisterModeAvailable method [Microsoft Broadband Networks], OnRegisterModeAvailable method [Microsoft Broadband Networks],IMbnRegistrationEvents interface, mbn.imbnregistrationevents_onregistermodeavailable, mbnapi/IMbnRegistrationEvents::OnRegisterModeAvailable
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
 - IMbnRegistrationEvents::OnRegisterModeAvailable
 - mbnapi/IMbnRegistrationEvents::OnRegisterModeAvailable
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
 - IMbnRegistrationEvents.OnRegisterModeAvailable
---

# IMbnRegistrationEvents::OnRegisterModeAvailable


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method called by the Mobile Broadband service to indicate that registration mode information is available.

## -parameters

### -param newInterface [in]

Pointer to an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a> interface that represents the applicable device.

## -returns

This method must return <b>S_OK</b>.

## -remarks

The <b>OnRegisterModeAvailable</b> method is called by the Mobile Broadband service to signal that  the registration mode information for a device is available. An application can call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getregistermode">GetRegisterMode</a> method of the passed <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a> get the current registration mode of the device.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>