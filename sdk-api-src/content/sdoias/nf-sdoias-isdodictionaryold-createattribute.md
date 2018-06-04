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

# ISdoDictionaryOld::CreateAttribute


## -description


The 
<b>CreateAttribute</b> method creates a new attribute object and returns an 
<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface to it.


## -parameters




### -param Id [in]

Specifies a value from the enumeration type 
<a href="https://msdn.microsoft.com/42a74deb-6d6e-493a-b9e0-d9549a5530d3">ATTRIBUTEID</a>. This value specifies the type of attribute to create.


### -param ppAttributeObject [out]

Pointer to a pointer to an 
<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer for the created attribute object.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -see-also




<a href="https://msdn.microsoft.com/42a74deb-6d6e-493a-b9e0-d9549a5530d3">ATTRIBUTEID</a>



<a href="https://msdn.microsoft.com/5aaa4008-3b39-4d1d-90db-79631e5bb6b9">ISdoDictionaryOld</a>
 

 

