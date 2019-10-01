---
UID: NF:mbnapi.IMbnRegistration.GetPacketAttachNetworkError
title: IMbnRegistration::GetPacketAttachNetworkError (mbnapi.h)
author: windows-sdk-content
description: Gets the network error from a packet attach operation.
old-location: mbn\imbnregistration_getpacketattachnetworkerror.htm
tech.root: mbn
ms.assetid: b51103fe-f4b2-46a5-9335-44bf6591e447
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPacketAttachNetworkError, GetPacketAttachNetworkError method [Microsoft Broadband Networks], GetPacketAttachNetworkError method [Microsoft Broadband Networks],IMbnRegistration interface, IMbnRegistration interface [Microsoft Broadband Networks],GetPacketAttachNetworkError method, IMbnRegistration.GetPacketAttachNetworkError, IMbnRegistration::GetPacketAttachNetworkError, mbn.imbnregistration_getpacketattachnetworkerror, mbnapi/IMbnRegistration::GetPacketAttachNetworkError
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnRegistration.GetPacketAttachNetworkError"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnRegistration.GetPacketAttachNetworkError
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnRegistration::GetPacketAttachNetworkError


## -description


Gets the network error from a packet attach operation.


## -parameters




### -param packetAttachNetworkError [out]

A pointer to an error code returned by the last failed network packet attach operation.  This is set to 0 if there is no error or if the error code is unknown.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For GSM devices, the error codes are defined in 3GPP specification 24.008 as "cause codes".  For CDMA devices, the codes are device and network specific.

The error codes are cleared when the packet attach operation completes successfully.

Whenever there is a change in the network error value, the Mobile Broadband service will call the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onpacketservicestatechange">OnPacketServiceStateChange</a> method of <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a>
 

 

