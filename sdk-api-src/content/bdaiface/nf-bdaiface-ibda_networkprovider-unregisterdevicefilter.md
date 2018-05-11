---
UID: NF:bdaiface.IBDA_NetworkProvider.UnRegisterDeviceFilter
title: IBDA_NetworkProvider::UnRegisterDeviceFilter
author: windows-driver-content
description: The UnRegisterDeviceFilter method is called by BDA device filters when they are removed from the filter graph.
old-location: mstv\ibda_networkprovider_unregisterdevicefilter.htm
old-project: mstv
ms.assetid: 7d54830f-93cc-44c0-9bb7-43c439f4aa8e
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IBDA_NetworkProvider interface [Microsoft TV Technologies],UnRegisterDeviceFilter method, IBDA_NetworkProvider.UnRegisterDeviceFilter, IBDA_NetworkProvider::UnRegisterDeviceFilter, IBDA_NetworkProviderUnRegisterDeviceFilter, UnRegisterDeviceFilter, UnRegisterDeviceFilter method [Microsoft TV Technologies], UnRegisterDeviceFilter method [Microsoft TV Technologies],IBDA_NetworkProvider interface, bdaiface/IBDA_NetworkProvider::UnRegisterDeviceFilter, mstv.ibda_networkprovider_unregisterdevicefilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_NetworkProvider.UnRegisterDeviceFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_NetworkProvider::UnRegisterDeviceFilter


## -description



The <b>UnRegisterDeviceFilter</b> method is called by BDA device filters when they are removed from the filter graph.




## -parameters




### -param pvRegistrationContext






#### - ulRegistrationContext [in]

The registration context that the filter received in the call to <b>RegisterDeviceFilter</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/84b6cd51-4cb5-4a43-9ac2-88ca8049b950">IBDA_NetworkProvider Interface</a>
 

 

