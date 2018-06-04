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

# IStorage::EnumElements


## -description



			The <b>EnumElements</b> method retrieves a pointer to an enumerator object that can be used to enumerate the storage and stream objects contained within this storage object.


## -parameters




### -param reserved1 [in]

Reserved for future use; must be zero.


### -param reserved2 [in]

Reserved for future use; must be <b>NULL</b>.


### -param reserved3 [in]

Reserved for future use; must be zero.


### -param ppenum [out]

Pointer to 
<a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a>* pointer variable that receives the interface pointer to the new enumerator object.


## -returns



This method can return one of these values.




## -remarks



The enumerator object returned by this method implements the 
<a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a> interface, one of the standard enumerator interfaces that contain the <b>Next</b>, <b>Reset</b>, 
<b>Clone</b>, and <b>Skip</b> methods. 
<b>IEnumSTATSTG</b> enumerates the data stored in an array of 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures.

The storage object must be open in read mode to allow the enumeration of its elements.

The order in which the elements are enumerated and whether the enumerator is a snapshot or always reflects the current state of the storage object, and depends on the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> implementation.




## -see-also




<a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a>



<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a>
 

 

