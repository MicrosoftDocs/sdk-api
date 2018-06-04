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

# IObjectConstruct::Construct


## -description


Constructs an object using the specified parameters.


## -parameters




### -param pCtorObj [in]

A reference to an implementation of the <a href="https://msdn.microsoft.com/ebfa8384-1efd-4775-b66f-b8048af33abc">IObjectConstructString</a> interface. 


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/5e630812-b2cf-4512-af67-6e919a02bf95">COM+ Object Constructor Strings</a>



<a href="https://msdn.microsoft.com/3fc84c37-f38d-4ff1-bdb1-f5d298802b64">IObjectConstruct</a>



<a href="https://msdn.microsoft.com/ebfa8384-1efd-4775-b66f-b8048af33abc">IObjectConstructString</a>



<a href="https://msdn.microsoft.com/0c5aaaae-368e-4b3e-a483-b3a23c353e6e">Specifying an Object Constructor String for a Component</a>
 

 

