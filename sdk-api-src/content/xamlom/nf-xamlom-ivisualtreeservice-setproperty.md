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

# IVisualTreeService::SetProperty


## -description


Sets a property value on a XAML element.


## -parameters




### -param instanceHandle [in]

A handle to the element to set the property on.


### -param value [in]

A handle to the value to set on the element property.


### -param propertyIndex [in]

The index (in the XAML runtime cache) of the property to set.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The caller of <b>SetProperty</b> must know the index of the property to be set by first calling
    <a href="https://msdn.microsoft.com/3D997B09-7B20-47BC-B19C-98945CA41D17">GetPropertyValuesChain</a> and finding the property they want to set and retrieving its index.
    They must also have an <b>InstanceHandle</b> to a value, either by calling <a href="https://msdn.microsoft.com/214BE795-5883-4761-9040-2C7A679F5258">CreateInstance</a>, or caching
    an earlier instance of some shared property, such as <b>SolidColorBrush</b>.




## -see-also




<a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService</a>
 

 

