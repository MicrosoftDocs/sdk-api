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

# IPropertyStorage::SetClass


## -description



			The <b>SetClass</b> method assigns a new CLSID to the current property storage object, and persistently stores the CLSID with the object.


## -parameters




### -param clsid [in]

New CLSID to be associated with the property set.


## -returns




						This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



Assigns a CLSID to the current property storage object. The CLSID has no relationship to the stored property IDs. Assigning a CLSID allows a piece of code to be associated with a given instance of a property set; such code, for example, might manage the user interface (UI). Different CLSIDs can be associated with different property set instances that have the same FMTID.

If the property set is created with the <i>pclsid</i> parameter of the <a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a> method specified as <b>NULL</b>, the CLSID is set to all zeroes.

The current CLSID on a property storage object can be retrieved with a call to 
<a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">IPropertyStorage::Stat</a>. The initial value for the CLSID can be specified at the time that the storage is created with a call to <a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a>.

Setting the CLSID on a nonsimple property set (one that can legally contain storage- or stream-valued properties, as described in <a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a>) also sets the CLSID on the underlying sub-storage.




## -see-also




<a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a>



<a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">IPropertyStorage::Stat</a>
 

 

