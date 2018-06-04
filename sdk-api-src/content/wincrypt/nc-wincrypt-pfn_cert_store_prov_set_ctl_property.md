---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# PFN_CERT_STORE_PROV_SET_CTL_PROPERTY callback function


## -description



			The <b>CertStoreProvSetCTLProperty</b> callback function determines whether a property can be set on a CTL. It is called by 
<a href="https://msdn.microsoft.com/3af01ca6-6fa1-4510-872a-b5e13e07f49f">CertSetCTLContextProperty</a> before setting a CTL's property. It can also be called by 
<a href="https://msdn.microsoft.com/16e45fe1-2710-4fa1-82da-c298645d7379">CertGetCTLContextProperty</a>, when getting a hash property that needs to be created and then persisted. This callback function does not set the 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>'s property.


## -parameters




### -param hStoreProv [in]

A handle to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.


### -param pCtlContext [in]

A pointer to a 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure.


### -param dwPropId [in]

Identifier of the property to be set.


### -param dwFlags [in]

Any needed flag values.


### -param *pvData [in]

A pointer to a buffer containing the property value to be set.


## -returns




						Returns <b>TRUE</b> if the property can be set. Returns <b>FALSE</b> if the property cannot be set.




## -see-also




<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/16e45fe1-2710-4fa1-82da-c298645d7379">CertGetCTLContextProperty</a>



<a href="https://msdn.microsoft.com/3af01ca6-6fa1-4510-872a-b5e13e07f49f">CertSetCTLContextProperty</a>
 

 

