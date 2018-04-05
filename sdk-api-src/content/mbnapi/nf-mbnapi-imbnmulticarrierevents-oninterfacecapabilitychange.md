---
UID: NF:mbnapi.IMbnMultiCarrierEvents.OnInterfaceCapabilityChange
title: IMbnMultiCarrierEvents::OnInterfaceCapabilityChange method
author: windows-driver-content
description: This notification method is called by the Mobile Broadband service to indicate the completion of a SetHomeProvider operation that updates the interface capabilities.
old-location: mbn\imbnmulticarrierevents_oninterfacecapabilitychange.htm
old-project: mbn
ms.assetid: 5701E0EB-FBDC-4791-97AA-B31F87763854
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnMultiCarrierEvents, IMbnMultiCarrierEvents interface [Microsoft Broadband Networks], OnInterfaceCapabilityChange method, IMbnMultiCarrierEvents::OnInterfaceCapabilityChange, OnInterfaceCapabilityChange method [Microsoft Broadband Networks], OnInterfaceCapabilityChange method [Microsoft Broadband Networks], IMbnMultiCarrierEvents interface, OnInterfaceCapabilityChange,IMbnMultiCarrierEvents.OnInterfaceCapabilityChange, mbn.imbnmulticarrierevents_oninterfacecapabilitychange, mbnapi/IMbnMultiCarrierEvents::OnInterfaceCapabilityChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnMultiCarrierEvents.OnInterfaceCapabilityChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnMultiCarrierEvents::OnInterfaceCapabilityChange method


## -description


This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://msdn.microsoft.com/9FDC1B01-4768-4621-9B0E-6EC9AB4275A9">SetHomeProvider</a> operation that updates the interface capabilities.


## -parameters




### -param mbnInterface [in]

An <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a> object that represents the Mobile Broadband device.


## -returns



This method must return <b>S_OK</b>.




## -remarks



When a network carrier is changed due to a call to <a href="https://msdn.microsoft.com/9FDC1B01-4768-4621-9B0E-6EC9AB4275A9">SetHomeProvider</a>, <b>OnInterfaceCapabilityChange</b>  is called when the interface capabilities are updated with the capabilities of the new carrier. An application can then call the <a href="https://msdn.microsoft.com/cfe8f638-ad17-4118-9c79-b7ebc81c726a">GetInterfaceCapability</a> method of the <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> object passed to <b>SetHomeProvider</b> to get the available capability information. The <b>IMbnInterface</b> can be retrieved by calling <b>QueryInterface</b>on the <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a> object passed to <b>OnInterfaceCapabilityChange</b>. For a list of interface capabilities, see <a href="https://msdn.microsoft.com/faee7f53-b465-4240-b163-ce88fae764df">MBN_INTERFACE_CAPS</a>.




## -see-also




<a href="https://msdn.microsoft.com/F7CAF21B-F487-4F35-806B-312B5246C1B2">IMbnMultiCarrierEvents</a>
 

 

