---
UID: NF:mbnapi.IMbnInterfaceEvents.OnInterfaceCapabilityAvailable
title: IMbnInterfaceEvents::OnInterfaceCapabilityAvailable (mbnapi.h)
description: This notification method is called by the Mobile Broadband service to indicate that interface capability information is available.
helpviewer_keywords: ["IMbnInterfaceEvents interface [Microsoft Broadband Networks]","OnInterfaceCapabilityAvailable method","IMbnInterfaceEvents.OnInterfaceCapabilityAvailable","IMbnInterfaceEvents::OnInterfaceCapabilityAvailable","OnInterfaceCapabilityAvailable","OnInterfaceCapabilityAvailable method [Microsoft Broadband Networks]","OnInterfaceCapabilityAvailable method [Microsoft Broadband Networks]","IMbnInterfaceEvents interface","mbn.imbninterfaceevents_oninterfacecapabilityavailable","mbnapi/IMbnInterfaceEvents::OnInterfaceCapabilityAvailable"]
old-location: mbn\imbninterfaceevents_oninterfacecapabilityavailable.htm
tech.root: mbn
ms.assetid: eeeffe13-307b-45f3-aa24-c33c621aa18e
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnInterfaceCapabilityAvailable method, IMbnInterfaceEvents.OnInterfaceCapabilityAvailable, IMbnInterfaceEvents::OnInterfaceCapabilityAvailable, OnInterfaceCapabilityAvailable, OnInterfaceCapabilityAvailable method [Microsoft Broadband Networks], OnInterfaceCapabilityAvailable method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_oninterfacecapabilityavailable, mbnapi/IMbnInterfaceEvents::OnInterfaceCapabilityAvailable
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
 - IMbnInterfaceEvents::OnInterfaceCapabilityAvailable
 - mbnapi/IMbnInterfaceEvents::OnInterfaceCapabilityAvailable
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
 - IMbnInterfaceEvents.OnInterfaceCapabilityAvailable
---

# IMbnInterfaceEvents::OnInterfaceCapabilityAvailable


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification method is called by the Mobile Broadband service to indicate that interface capability information is available.

## -parameters

### -param newInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> whose capability information has become available.

## -returns

This method must return <b>S_OK</b>.

## -remarks

The application can issue the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getinterfacecapability">GetInterfaceCapability</a> method  of the passed <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> to get the available capability information. For a list of interface capabilities, see <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a>

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>