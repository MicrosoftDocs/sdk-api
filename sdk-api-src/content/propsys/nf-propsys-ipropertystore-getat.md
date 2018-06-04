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

# IPropertyStore::GetAt


## -description


Gets a property key from the property array of an item.


## -parameters




### -param iProp

The index of the property key in the array of PROPERTYKEY structures. This is a zero-based index.


### -param pkey






#### - pKey

A pointer to a PROPERTYKEY structure and it can be used in subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536962">IPropertyStore::GetValue</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff536963">IPropertyStore::SetValue</a>.


## -returns



The <code>IPropertyStore::GetAt</code> method returns a value of S_OK if successful. Otherwise, any other code it returns must be considered to be an error code.




## -remarks



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536962">IPropertyStore::GetValue</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536963">IPropertyStore::SetValue</a>
 

 

