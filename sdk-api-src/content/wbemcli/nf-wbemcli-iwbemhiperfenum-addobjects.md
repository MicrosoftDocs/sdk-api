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

# IWbemHiPerfEnum::AddObjects


## -description


The <b>IWbemHiPerfEnum::AddObjects</b> method adds the supplied instance objects to the enumerator.


## -parameters




### -param lFlags

Reserved. This parameter must be 0.


### -param uNumObjects [in]

Number of items in the object and the number of identifiers in the parameter.


### -param apIds [in]

Pointer to an array of integers that contains a unique identifier for each object in the object array.


### -param apObj [in]

Pointer to an array of instance objects to add to the enumerator.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -remarks



If an identifier already exists, <b>WBEM_E_FAILED</b> is returned. The refresher identifiers can be used to remove objects later.




## -see-also




<a href="https://msdn.microsoft.com/71ce1c89-446e-4137-9857-9d3c5921e0b7">IWbemHiPerfEnum</a>
 

 

