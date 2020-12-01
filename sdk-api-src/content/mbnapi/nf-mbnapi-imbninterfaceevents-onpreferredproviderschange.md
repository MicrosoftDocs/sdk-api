---
UID: NF:mbnapi.IMbnInterfaceEvents.OnPreferredProvidersChange
title: IMbnInterfaceEvents::OnPreferredProvidersChange (mbnapi.h)
description: This notification method is called by the Mobile Broadband service to indicate a change in a device's preferred provider list.
helpviewer_keywords: ["IMbnInterfaceEvents interface [Microsoft Broadband Networks]","OnPreferredProvidersChange method","IMbnInterfaceEvents.OnPreferredProvidersChange","IMbnInterfaceEvents::OnPreferredProvidersChange","OnPreferredProvidersChange","OnPreferredProvidersChange method [Microsoft Broadband Networks]","OnPreferredProvidersChange method [Microsoft Broadband Networks]","IMbnInterfaceEvents interface","mbn.imbninterfaceevents_onpreferredproviderschange","mbnapi/IMbnInterfaceEvents::OnPreferredProvidersChange"]
old-location: mbn\imbninterfaceevents_onpreferredproviderschange.htm
tech.root: mbn
ms.assetid: ccede3de-4dfd-469f-afb4-d1424c56c7bc
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnPreferredProvidersChange method, IMbnInterfaceEvents.OnPreferredProvidersChange, IMbnInterfaceEvents::OnPreferredProvidersChange, OnPreferredProvidersChange, OnPreferredProvidersChange method [Microsoft Broadband Networks], OnPreferredProvidersChange method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_onpreferredproviderschange, mbnapi/IMbnInterfaceEvents::OnPreferredProvidersChange
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
 - IMbnInterfaceEvents::OnPreferredProvidersChange
 - mbnapi/IMbnInterfaceEvents::OnPreferredProvidersChange
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
 - IMbnInterfaceEvents.OnPreferredProvidersChange
---

# IMbnInterfaceEvents::OnPreferredProvidersChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification method is called by the Mobile Broadband service to indicate a change in a device's preferred provider list.

## -parameters

### -param newInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents the Mobile Broadband device whose preferred provider list has changed.

## -returns

This method must return <b>S_OK</b>.

## -remarks

In some cases, a device's preferred provider list can be updated by the network by SMS or OTA (over The air) update. The Mobile Broadband service will call this method to notify the application about any change in the preferred provider list. The application can call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getpreferredproviders">GetPreferredProviders</a> method of the passed <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> to get the updated list of preferred providers.


If there is a change in the preferred provider list because of a call to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-setpreferredproviders">SetPreferredProviders</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>, then this notification will not be called.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>