---
UID: NF:mbnapi.IMbnConnection.GetActivationNetworkError
title: IMbnConnection::GetActivationNetworkError
author: windows-sdk-content
description: Gets the network error returned in a Packet Data Protocol (PDP) context activation failure.
old-location: mbn\imbnconnection_getactivationnetworkerror.htm
tech.root: mbn
ms.assetid: a8bda00b-5eff-46a4-b640-1794e8ea21cf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetActivationNetworkError, GetActivationNetworkError method [Microsoft Broadband Networks], GetActivationNetworkError method [Microsoft Broadband Networks],IMbnConnection interface, IMbnConnection interface [Microsoft Broadband Networks],GetActivationNetworkError method, IMbnConnection.GetActivationNetworkError, IMbnConnection::GetActivationNetworkError, mbn.imbnconnection_getactivationnetworkerror, mbnapi/IMbnConnection::GetActivationNetworkError
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMbnConnection.GetActivationNetworkError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnConnection::GetActivationNetworkError


## -description


Gets the network error returned in a Packet Data Protocol (PDP) context activation failure.


## -parameters




### -param networkError [out, retval]

The error code returned by the network from the last connection context activation operation.  The value is meaningful only if the method returns <b>S_OK</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For GSM devices these error codes are defined in 3GPP specification 24.008 as cause codes. For CDMA devices, device and network specific error codes are used.

The error codes are cleared when the context activation operation completes successfully. When there is no network error or the error is not known, then the value is set to 0.

Whenever there is a change in the network error value, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/5392e5b7-eac7-40f1-b5cd-adde5a6ff1b8">OnConnectStateChange</a> member of <a href="https://msdn.microsoft.com/9135ba2e-62f6-495e-b136-9efc5f260581">IMbnConnectionEvents</a>.





## -see-also




<a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a>
 

 

