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

# PD2D1_PROPERTY_SET_FUNCTION callback function


## -description


Sets a property on an effect.


## -parameters




### -param *effect [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface for the effect on which the property will be set.


### -param *data [in]

A pointer to the data to be set on the property.


### -param dataSize

The number of bytes in the property set by the function.


## -returns



Returns S_OK if successful; otherwise, returns an <b>HRESULT</b> error code.




## -remarks



Supply a <b>PD2D1_PROPERTY_SET_FUNCTION</b> function pointer to the <b>setFunction</b> member of a <a href="https://msdn.microsoft.com/0eb6d428-cb65-4738-9cf3-64038b728004">D2D1_PROPERTY_BINDING</a> structure to specify the function that Direct2D uses to set data for a property.




## -see-also




<a href="https://msdn.microsoft.com/0eb6d428-cb65-4738-9cf3-64038b728004">D2D1_PROPERTY_BINDING</a>
 

 

