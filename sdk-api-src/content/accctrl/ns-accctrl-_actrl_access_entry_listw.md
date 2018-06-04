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

# _ACTRL_ACCESS_ENTRY_LISTW structure


## -description


Contains a list of access entries.


## -struct-fields




### -field cEntries

The number of entries in the <b>pAccessList</b> array.


### -field pAccessList

A pointer to an array of <a href="https://msdn.microsoft.com/bcb2ad72-7b00-4582-b05e-e00720a4db77">ACTRL_ACCESS_ENTRY</a> structures. Each structure specifies access-control information for a specified trustee. 



### -field pAccessList.size_is

 


### -field pAccessList.size_is.cEntries

 




## -remarks



To create an empty access list, set <b>cEntries</b> to zero and <b>pAccessList</b> to <b>NULL</b>. An empty list does not grant access to any trustee, and thus, denies all access to an object.

To create a null access list, set the <b>pAccessEntryList</b> member of the <a href="https://msdn.microsoft.com/90b13dd1-0ca6-4674-b9fa-a61aed4637d7">ACTRL_PROPERTY_ENTRY</a> structure to <b>NULL</b>. A null access list grants everyone full access to the object.




## -see-also




<a href="https://msdn.microsoft.com/90b13dd1-0ca6-4674-b9fa-a61aed4637d7">ACTRL_PROPERTY_ENTRY</a>
 

 

