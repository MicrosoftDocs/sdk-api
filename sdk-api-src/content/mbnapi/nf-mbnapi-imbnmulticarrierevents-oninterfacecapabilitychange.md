---
UID: NF:mbnapi.IMbnMultiCarrierEvents.OnInterfaceCapabilityChange
title: IMbnMultiCarrierEvents::OnInterfaceCapabilityChange (mbnapi.h)
description: This notification method is called by the Mobile Broadband service to indicate the completion of a SetHomeProvider operation that updates the interface capabilities.
helpviewer_keywords: ["IMbnMultiCarrierEvents interface [Microsoft Broadband Networks]","OnInterfaceCapabilityChange method","IMbnMultiCarrierEvents.OnInterfaceCapabilityChange","IMbnMultiCarrierEvents::OnInterfaceCapabilityChange","OnInterfaceCapabilityChange","OnInterfaceCapabilityChange method [Microsoft Broadband Networks]","OnInterfaceCapabilityChange method [Microsoft Broadband Networks]","IMbnMultiCarrierEvents interface","mbn.imbnmulticarrierevents_oninterfacecapabilitychange","mbnapi/IMbnMultiCarrierEvents::OnInterfaceCapabilityChange"]
old-location: mbn\imbnmulticarrierevents_oninterfacecapabilitychange.htm
tech.root: mbn
ms.assetid: 5701E0EB-FBDC-4791-97AA-B31F87763854
ms.date: 12/05/2018
ms.keywords: IMbnMultiCarrierEvents interface [Microsoft Broadband Networks],OnInterfaceCapabilityChange method, IMbnMultiCarrierEvents.OnInterfaceCapabilityChange, IMbnMultiCarrierEvents::OnInterfaceCapabilityChange, OnInterfaceCapabilityChange, OnInterfaceCapabilityChange method [Microsoft Broadband Networks], OnInterfaceCapabilityChange method [Microsoft Broadband Networks],IMbnMultiCarrierEvents interface, mbn.imbnmulticarrierevents_oninterfacecapabilitychange, mbnapi/IMbnMultiCarrierEvents::OnInterfaceCapabilityChange
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMbnMultiCarrierEvents::OnInterfaceCapabilityChange
 - mbnapi/IMbnMultiCarrierEvents::OnInterfaceCapabilityChange
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
 - IMbnMultiCarrierEvents.OnInterfaceCapabilityChange
---

# IMbnMultiCarrierEvents::OnInterfaceCapabilityChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-sethomeprovider">SetHomeProvider</a> operation that updates the interface capabilities.

## -parameters

### -param mbnInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrier">IMbnMultiCarrier</a> object that represents the Mobile Broadband device.

## -returns

This method must return <b>S_OK</b>.

## -remarks

When a network carrier is changed due to a call to <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-sethomeprovider">SetHomeProvider</a>, <b>OnInterfaceCapabilityChange</b>  is called when the interface capabilities are updated with the capabilities of the new carrier. An application can then call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getinterfacecapability">GetInterfaceCapability</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> object passed to <b>SetHomeProvider</b> to get the available capability information. The <b>IMbnInterface</b> can be retrieved by calling <b>QueryInterface</b> on the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrier">IMbnMultiCarrier</a> object passed to <b>OnInterfaceCapabilityChange</b>. For a list of interface capabilities, see <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrierevents">IMbnMultiCarrierEvents</a>