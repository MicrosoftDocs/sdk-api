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

# IContextProperties::EnumNames


## -description


Retrieves a reference to an enumerator for the context object properties.


## -parameters




### -param ppenum [out]

A reference to the <a href="https://msdn.microsoft.com/9f70b554-3cdd-4a4b-b180-c6de6182a46a">IEnumNames</a> interface on a new enumerator object that you can use to iterate through all the context object properties.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



Use the <b>EnumNames</b> method to obtain a reference to an enumerator object. The returned <a href="https://msdn.microsoft.com/9f70b554-3cdd-4a4b-b180-c6de6182a46a">IEnumNames</a> interface exposes several methods you can use to iterate through a list of <b>BSTR</b> values representing context object properties. When you have a name, you can use the <a href="https://msdn.microsoft.com/dc7748b4-5cf4-41c6-af7d-82b2478b084c">GetProperty</a> method to obtain a reference to the context object property it represents. As with any COM object, you must release an enumerator object when you are finished using it.




## -see-also




<a href="https://msdn.microsoft.com/95a5cfda-7587-496e-ba16-0dd2e8a4db32">IContextProperties</a>
 

 

