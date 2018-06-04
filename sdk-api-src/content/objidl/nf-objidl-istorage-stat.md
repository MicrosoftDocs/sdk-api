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

# IStorage::Stat


## -description



			The <b>Stat</b> method retrieves the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure for this open storage object.


## -parameters




### -param pstatstg [out]

On return, pointer to a 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure where this method places information about the open storage object. This parameter is <b>NULL</b> if an error occurs.


### -param grfStatFlag [in]

Specifies that some of the members in the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure are not returned, thus saving a memory allocation operation. Values are taken from the 
<a href="https://msdn.microsoft.com/9070b517-8ca5-455f-baee-0647b1895c08">STATFLAG</a> enumeration.


## -returns



This method can return one of these values.




## -remarks



<b>IStorage::Stat</b> retrieves the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure for the current storage object. The 
<b>STATSTG</b> structure contains statistical information about the storage object. <a href="https://msdn.microsoft.com/29ca157e-40e2-4e9a-95fb-a31bb45570f2">IStorage::EnumElements</a> returns a pointer to an enumerator object. The enumerator object returned by this method implements the 
<a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a> interface, through which the data stored in the array of the 
<b>STATSTG</b> structures is enumerated.




## -see-also




<a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a>



<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/02ab2708-fc8b-4941-939a-a819cf823108">IStorage::SetClass</a>



<a href="https://msdn.microsoft.com/f6a1fba4-0444-4de3-a838-2d339878fe24">IStorage::SetElementTimes</a>



<a href="https://msdn.microsoft.com/52606df8-10ea-40e7-bb61-c86c7b7262d2">IStorage::SetStateBits</a>



<a href="https://msdn.microsoft.com/9070b517-8ca5-455f-baee-0647b1895c08">STATFLAG</a>



<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a>
 

 

