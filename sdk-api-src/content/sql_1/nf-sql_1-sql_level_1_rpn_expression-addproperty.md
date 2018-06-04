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

# AddProperty function


## -description


The <b>AddProperty</b> function adds one property to the parser <a href="p.htm">property database</a>.


## -parameters




### -param pProp

TBD




#### - PropertyInfo [in]

Pointer to a 
<a href="https://msdn.microsoft.com/878777ab-141d-4cc5-b0c1-f2ac8f770bf0">PROPERTYINFO</a> structure that defines the property.


#### - hProtocol [in]

Handle of the protocol that is associated with the database. When Network Monitor calls the 
<a href="https://msdn.microsoft.com/b8a2752d-30a6-48f2-90b3-b1430ae983d2">Register</a> function, Network Monitor passes the protocol handle to the parser DLL.


## -returns



If the function is successful, the return value is a pointer to the property that is added.

If the function is unsuccessful, the return value is <b>NULL</b>.




## -remarks



The <b>AddProperty</b> function should be called only when implementing the 
<a href="https://msdn.microsoft.com/b8a2752d-30a6-48f2-90b3-b1430ae983d2">Register</a> function. The parser uses <b>AddProperty</b> to add a property to the <a href="p.htm">property database</a> of the protocol. Properties are added to the database one property at a time.

<b>AddProperty</b> must be called after calling 
<a href="https://msdn.microsoft.com/0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69">CreatePropertyDatabase</a>. If <b>AddProperty</b> is called before the property database is created, Network Monitor returns the NMERR_NO_PROPERTY_DATABASE error.




## -see-also




<a href="https://msdn.microsoft.com/0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69">CreatePropertyDatabase</a>



<a href="https://msdn.microsoft.com/878777ab-141d-4cc5-b0c1-f2ac8f770bf0">PROPERTYINFO</a>



<a href="https://msdn.microsoft.com/b8a2752d-30a6-48f2-90b3-b1430ae983d2">Register</a>
 

 

