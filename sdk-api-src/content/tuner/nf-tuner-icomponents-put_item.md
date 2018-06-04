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

# IComponents::put_Item


## -description



The <b>put_Item</b> method inserts a component into the collection, replacing the item that is identified by the specified index.




## -parameters




### -param Index [in]

Specifies the index to assign to the component. This parameter is a value of type <b>VARIANT</b>.


### -param ppComponent






#### - pComponent [in]

Pointer to the <a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent</a> interface of the component object. The method creates a clone of the component and inserts the clone into the collection.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method allows the client to replace an existing item in the collection.

If the collection contains <i>n</i> items, valid indexes are in the range 0 to <i>n</i>-1. To determine the number of items in the collection, call <a href="https://msdn.microsoft.com/ba198e27-c699-4c93-aa2d-b8be8c40380c">get_Count</a>.




## -see-also




<a href="https://msdn.microsoft.com/670b47ba-bcbd-4281-95e3-a5d784f0610b">IComponents Interface</a>



<a href="https://msdn.microsoft.com/12716c7c-3156-401e-8f1c-be3100afb912">get_Item</a>
 

 

