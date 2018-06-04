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

# ISdoCollection::Item


## -description


The 
<b>Item</b> method retrieves the specified item from the collection.


## -parameters




### -param Name [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>. Store the name of the object in a 
<a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> in this <b>VARIANT</b>.


### -param pItem [out]

Pointer to an interface pointer that receives the address of an 
<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface for the object.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the object is not found in the collection, the return value is <b>DISP_E_MEMBERNOTFOUND</b>.

Otherwise, if the method fails, the return value is one of the following error codes.




## -remarks



Neither of the parameters can be <b>NULL</b>.




## -see-also




<a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>



<a href="https://msdn.microsoft.com/9c7ee4d7-987f-45ae-810f-fc310955f36d">IASCOMMONPROPERTIES</a>



<a href="https://msdn.microsoft.com/26470906-1cba-41fc-96f3-078208ab3d51">ISdoCollection</a>



<a href="https://msdn.microsoft.com/df7cbff5-2d09-4031-8f41-3f4eea51598f">Retrieving an Object from a Collection</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>
 

 

