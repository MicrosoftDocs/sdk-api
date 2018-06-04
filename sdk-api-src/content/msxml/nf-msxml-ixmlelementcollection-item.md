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

# IXMLElementCollection::item


## -description


Retrieves the child elements from a collection using their index, name, or both.


## -parameters




### -param var1 [in, optional]

A valid index numeric value (within the length of <a href="https://msdn.microsoft.com/1d27e5fc-0491-44ee-9134-40f9f909b1cb">IXMLElementCollection</a>) or the name of an element in the XML hierarchy.


### -param var2 [in, optional]

A valid index numeric value (within the length of <a href="https://msdn.microsoft.com/1d27e5fc-0491-44ee-9134-40f9f909b1cb">IXMLElementCollection</a>) or the name of an element in the XML hierarchy.


### -param ppDisp






## -returns



Returns an <b>IDispatch</b> pointer to an addressable memory location where the collection is retrievable.




## -remarks



This method is implemented in MSXML 1.0. It is no longer supported by Microsoft in current versions of MSXML. This documentation is provided for informational purposes only.




## -see-also




<a href="https://msdn.microsoft.com/1d27e5fc-0491-44ee-9134-40f9f909b1cb">IXMLElementCollection</a>
 

 

