---
UID: NF:mbnapi.IMbnRegistration.GetRegistrationNetworkError
title: IMbnRegistration::GetRegistrationNetworkError
author: windows-sdk-content
description: Gets the network error from a registration operation.
old-location: mbn\imbnregistration_getregistrationnetworkerror.htm
old-project: mbn
ms.assetid: b0e6df7a-7b47-4587-92c2-f01fd96e768f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetRegistrationNetworkError, GetRegistrationNetworkError method [Microsoft Broadband Networks], GetRegistrationNetworkError method [Microsoft Broadband Networks],IMbnRegistration interface, IMbnRegistration interface [Microsoft Broadband Networks],GetRegistrationNetworkError method, IMbnRegistration.GetRegistrationNetworkError, IMbnRegistration::GetRegistrationNetworkError, mbn.imbnregistration_getregistrationnetworkerror, mbnapi/IMbnRegistration::GetRegistrationNetworkError
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnRegistration.GetRegistrationNetworkError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnRegistration::GetRegistrationNetworkError


## -description


Gets the network error from a registration operation.


## -parameters




### -param registrationNetworkError [out]

A pointer to an error code returned by the last failed network registration operation.  This is set to 0 if there is no error or if the error code is unknown.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For GSM devices, the error codes are defined in 3GPP specification 24.008 as "cause codes".  For CDMA devices, the codes are device and network specific.

The error codes are cleared when the packet attach operation completes successfully.

Whenever there is a change in the network error value, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/62393a9b-70e5-4819-8df1-59b94c1b6922">OnRegisterStateChange</a> method of <a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>.




## -see-also




<a href="https://msdn.microsoft.com/da5413b7-adf4-4a3d-893f-f51441460541">IMbnRegistration</a>
 

 

