---
UID: NF:mbnapi.IMbnRegistration.GetRegistrationNetworkError
title: IMbnRegistration::GetRegistrationNetworkError (mbnapi.h)
description: Gets the network error from a registration operation.
helpviewer_keywords: ["GetRegistrationNetworkError","GetRegistrationNetworkError method [Microsoft Broadband Networks]","GetRegistrationNetworkError method [Microsoft Broadband Networks]","IMbnRegistration interface","IMbnRegistration interface [Microsoft Broadband Networks]","GetRegistrationNetworkError method","IMbnRegistration.GetRegistrationNetworkError","IMbnRegistration::GetRegistrationNetworkError","mbn.imbnregistration_getregistrationnetworkerror","mbnapi/IMbnRegistration::GetRegistrationNetworkError"]
old-location: mbn\imbnregistration_getregistrationnetworkerror.htm
tech.root: mbn
ms.assetid: b0e6df7a-7b47-4587-92c2-f01fd96e768f
ms.date: 12/05/2018
ms.keywords: GetRegistrationNetworkError, GetRegistrationNetworkError method [Microsoft Broadband Networks], GetRegistrationNetworkError method [Microsoft Broadband Networks],IMbnRegistration interface, IMbnRegistration interface [Microsoft Broadband Networks],GetRegistrationNetworkError method, IMbnRegistration.GetRegistrationNetworkError, IMbnRegistration::GetRegistrationNetworkError, mbn.imbnregistration_getregistrationnetworkerror, mbnapi/IMbnRegistration::GetRegistrationNetworkError
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
 - IMbnRegistration::GetRegistrationNetworkError
 - mbnapi/IMbnRegistration::GetRegistrationNetworkError
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
 - IMbnRegistration.GetRegistrationNetworkError
---

# IMbnRegistration::GetRegistrationNetworkError


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the network error from a registration operation.

## -parameters

### -param registrationNetworkError [out]

A pointer to an error code returned by the last failed network registration operation.  This is set to 0 if there is no error or if the error code is unknown.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For GSM devices, the error codes are defined in 3GPP specification 24.008 as "cause codes".  For CDMA devices, the codes are device and network specific.

The error codes are cleared when the packet attach operation completes successfully.

Whenever there is a change in the network error value, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onregisterstatechange">OnRegisterStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a>