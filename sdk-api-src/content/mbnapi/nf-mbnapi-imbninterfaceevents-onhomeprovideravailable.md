---
UID: NF:mbnapi.IMbnInterfaceEvents.OnHomeProviderAvailable
title: IMbnInterfaceEvents::OnHomeProviderAvailable (mbnapi.h)
description: This notification method is called by the Mobile Broadband service to indicate that home provider information for the device is available.
helpviewer_keywords: ["IMbnInterfaceEvents interface [Microsoft Broadband Networks]","OnHomeProviderAvailable method","IMbnInterfaceEvents.OnHomeProviderAvailable","IMbnInterfaceEvents::OnHomeProviderAvailable","OnHomeProviderAvailable","OnHomeProviderAvailable method [Microsoft Broadband Networks]","OnHomeProviderAvailable method [Microsoft Broadband Networks]","IMbnInterfaceEvents interface","mbn.imbninterfaceevents_onhomeprovideravailable","mbnapi/IMbnInterfaceEvents::OnHomeProviderAvailable"]
old-location: mbn\imbninterfaceevents_onhomeprovideravailable.htm
tech.root: mbn
ms.assetid: 4da50033-d55c-4878-b05c-cbc43c156da0
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnHomeProviderAvailable method, IMbnInterfaceEvents.OnHomeProviderAvailable, IMbnInterfaceEvents::OnHomeProviderAvailable, OnHomeProviderAvailable, OnHomeProviderAvailable method [Microsoft Broadband Networks], OnHomeProviderAvailable method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_onhomeprovideravailable, mbnapi/IMbnInterfaceEvents::OnHomeProviderAvailable
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
 - IMbnInterfaceEvents::OnHomeProviderAvailable
 - mbnapi/IMbnInterfaceEvents::OnHomeProviderAvailable
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
 - IMbnInterfaceEvents.OnHomeProviderAvailable
---

# IMbnInterfaceEvents::OnHomeProviderAvailable


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification method is called by the Mobile Broadband service to indicate that home provider information for the device is available.

## -parameters

### -param newInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents the device whose home provider information has become available.

## -returns

This method must return <b>S_OK</b>.

## -remarks

An application can call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-gethomeprovider">GetHomeProvider</a> method of  the passed <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> to get the available home provider information.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>