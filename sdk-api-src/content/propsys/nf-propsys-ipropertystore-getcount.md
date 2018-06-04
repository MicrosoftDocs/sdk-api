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

# IPropertyStore::GetCount


## -description


This method returns a count of the number of properties that are attached to the file.


## -parameters




### -param cProps

A pointer to a value that indicates the property count.


## -returns



The <code>IpropertyStore::GetCount</code> method returns a value of S_OK when the call is successful, even if the file has no properties attached. Any other code returned is an error code.




## -remarks



<b>IPropertyStore</b> provides an abstraction over an array of property keys via the <code>IPropertyStore::GetCount</code> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a> methods. The property keys in this array represent the properties that are currently stored by the <b>IPropertyStore</b>.

When <code>GetCount</code> succeeds, the value pointed to by cProps is a count of property keys in the array. The caller can expect calls to <b>IPropertyStore::GetAt</b> to succeed for values of iProp less than cProps.

In the case of failures such as E_OUTOFMEMORY, you should set cProps to zero. It is preferable that errors are discovered during creation or initialization of the property store.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a>
 

 

