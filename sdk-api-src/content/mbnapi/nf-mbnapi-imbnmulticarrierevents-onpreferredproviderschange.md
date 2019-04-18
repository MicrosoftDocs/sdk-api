---
UID: NF:mbnapi.IMbnMultiCarrierEvents.OnPreferredProvidersChange
title: IMbnMultiCarrierEvents::OnPreferredProvidersChange (mbnapi.h)
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate the completion of a GetPreferredProviders operation and a change in a device's preferred provider list.
old-location: mbn\imbnmulticarrierevents_onpreferredproviderschange.htm
tech.root: mbn
ms.assetid: B2E7C42B-32B0-47D1-AA88-8A22B379B500
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnMultiCarrierEvents interface [Microsoft Broadband Networks],OnPreferredProvidersChange method, IMbnMultiCarrierEvents.OnPreferredProvidersChange, IMbnMultiCarrierEvents::OnPreferredProvidersChange, OnPreferredProvidersChange, OnPreferredProvidersChange method [Microsoft Broadband Networks], OnPreferredProvidersChange method [Microsoft Broadband Networks],IMbnMultiCarrierEvents interface, mbn.imbnmulticarrierevents_onpreferredproviderschange, mbnapi/IMbnMultiCarrierEvents::OnPreferredProvidersChange
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
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
 - IMbnMultiCarrierEvents.OnPreferredProvidersChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnMultiCarrierEvents::OnPreferredProvidersChange


## -description


This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://msdn.microsoft.com/91D27D4D-5838-4D6D-BECF-B336B9F3B52A">GetPreferredProviders</a> operation and a change in a device's preferred provider list.


## -parameters




### -param mbnInterface [in]


<a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a>


An <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a> object that represents the Mobile Broadband device <a href="https://msdn.microsoft.com/91D27D4D-5838-4D6D-BECF-B336B9F3B52A">GetPreferredProviders</a> operation.


## -returns



This method must return <b>S_OK</b>.




## -remarks



A device's preferred provider list can be updated by the network by SMS or OTA (over The air) update. The Mobile Broadband service will call this method to notify the application about any change in the preferred provider list. The application can call the <a href="https://msdn.microsoft.com/91D27D4D-5838-4D6D-BECF-B336B9F3B52A">GetPreferredProviders</a> method of the  <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a> object to get the updated list of preferred providers.




## -see-also




<a href="https://msdn.microsoft.com/F7CAF21B-F487-4F35-806B-312B5246C1B2">IMbnMultiCarrierEvents</a>
 

 

