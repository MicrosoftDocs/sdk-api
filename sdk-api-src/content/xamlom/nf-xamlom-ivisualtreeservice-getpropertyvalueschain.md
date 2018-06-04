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

# IVisualTreeService::GetPropertyValuesChain


## -description


Gets an array of all the
    properties set on the element passed in, and an array of all the styles involved in setting the effective values of the properties.


## -parameters




### -param instanceHandle [in]

A handle to the element to query properties on.


### -param pSourceCount [out]

The count of the property sources array.


### -param ppPropertySources [out]

An array of property sources.


### -param pPropertyCount [out]

The count of the property values array.


### -param ppPropertyValues [out]

An array of property values.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. This 
    method should not fail in normal conditions.




## -remarks



<b>GetPropertyValuesChain</b> returns an array of <a href="https://msdn.microsoft.com/111D10AB-2C16-4D21-A716-968C810B928F">PropertyChainValue</a> structs that represents all the
    properties set on the element passed in. It also returns an array of <a href="https://msdn.microsoft.com/B9A506D5-5F7B-429C-AA62-52B4C5BF78E0">PropertyChainSource</a> structs that represents all the styles involved in setting the effective value of each property. 




## -see-also




<a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService</a>
 

 

