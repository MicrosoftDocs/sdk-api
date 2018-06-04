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

# IADsCollection::Add


## -description


The <b>IADsCollection::Add</b> method adds a named item to the collection.


## -parameters




### -param bstrName [in]

The <b>BSTR</b> value that specifies the item name.  <a href="https://msdn.microsoft.com/04b33451-505e-43de-8db4-3e37f9909ea6">IADsCollection::GetObject</a> and  <a href="https://msdn.microsoft.com/21ce80fe-542b-4350-b66c-fa26f62ca611">IADsCollection::Remove</a> reference the item by this name.


### -param vItem






#### - varItem [in]

Item value. When the item is an object, this parameter holds the  <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer on the object.


## -returns



This method supports the standard return values, as well as the following.
      

For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



Collections for a directory service can also consist of a set of immutable objects.

This method is not supported in any of the  <a href="https://msdn.microsoft.com/419d7953-a879-4d6c-be74-173d76c3f932">ADSI system providers</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/419d7953-a879-4d6c-be74-173d76c3f932">ADSI System
  Providers</a>



<a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a>



<a href="https://msdn.microsoft.com/04b33451-505e-43de-8db4-3e37f9909ea6">IADsCollection::GetObject</a>



<a href="https://msdn.microsoft.com/21ce80fe-542b-4350-b66c-fa26f62ca611">IADsCollection::Remove</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

