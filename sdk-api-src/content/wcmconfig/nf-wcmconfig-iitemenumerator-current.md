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

# IItemEnumerator::Current


## -description


Retrieves an item from the current position of the enumerator.


## -parameters




### -param Item [out]

A variant that contains the key value for the collection. For most collections, the key is the name of the item.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -remarks



<div class="alert"><b>Note</b>  When the item is no longer required, call <a href="28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a> to free the resources associated with the item.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a>
 

 

