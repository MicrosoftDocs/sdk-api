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

# IOCSPPropertyCollection::GetAllProperties


## -description


The <b>GetAllProperties</b> method gets all properties in a property set.


## -parameters




### -param pVarProperties [out]

A pointer to a safe array that contains the properties as name-value pairs.

This array is a two-dimensional array of elements, each of type <b>VARIANT</b>. The array contains one row for each named property in the collection. Each row contains two columns: the property name and the property value.


## -returns



<h3>C++</h3>
If the method succeeds, it returns <b>S_OK</b>.


If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
A safe array that contains the properties as name-value pairs.

This array is a two-dimensional array of elements, each of type <b>Variant</b>. The array contains one row for each named property in the collection. Each row contains two columns: the property name and the property value.




## -see-also




<a href="https://msdn.microsoft.com/8c700357-0cb4-4780-9ff1-ac57c46f9183">IOCSPPropertyCollection</a>
 

 

