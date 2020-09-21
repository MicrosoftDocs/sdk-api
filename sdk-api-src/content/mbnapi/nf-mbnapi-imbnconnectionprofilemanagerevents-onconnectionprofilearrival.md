---
UID: NF:mbnapi.IMbnConnectionProfileManagerEvents.OnConnectionProfileArrival
title: IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival (mbnapi.h)
description: Notification method that indicates a new connection profile has been added to the system.
helpviewer_keywords: ["IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks]","OnConnectionProfileArrival method","IMbnConnectionProfileManagerEvents.OnConnectionProfileArrival","IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival","OnConnectionProfileArrival","OnConnectionProfileArrival method [Microsoft Broadband Networks]","OnConnectionProfileArrival method [Microsoft Broadband Networks]","IMbnConnectionProfileManagerEvents interface","mbn.imbnconnectionprofilemanagerevents_onconnectionprofilearrival","mbnapi/IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival"]
old-location: mbn\imbnconnectionprofilemanagerevents_onconnectionprofilearrival.htm
tech.root: mbn
ms.assetid: 94338c8c-2a89-412f-811e-5c50ecd9be70
ms.date: 12/05/2018
ms.keywords: IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks],OnConnectionProfileArrival method, IMbnConnectionProfileManagerEvents.OnConnectionProfileArrival, IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival, OnConnectionProfileArrival, OnConnectionProfileArrival method [Microsoft Broadband Networks], OnConnectionProfileArrival method [Microsoft Broadband Networks],IMbnConnectionProfileManagerEvents interface, mbn.imbnconnectionprofilemanagerevents_onconnectionprofilearrival, mbnapi/IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival
 - mbnapi/IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival
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
 - IMbnConnectionProfileManagerEvents.OnConnectionProfileArrival
---

# IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method that indicates a new connection profile has been added to the system.

## -parameters

### -param newConnectionProfile [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a> interface that represents a connection profile that has been added.

## -returns

This method must return <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanagerevents">IMbnConnectionProfileManagerEvents</a>