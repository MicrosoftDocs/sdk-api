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

# IStorage::SetElementTimes


## -description


The <b>SetElementTimes</b>  method sets the modification, access, and creation times of the specified storage element, if the underlying file system supports this method.


## -parameters




### -param pwcsName [in]

The name of the storage object element whose times are to be modified. If <b>NULL</b>, the time is set on the root storage rather than one of its elements.


### -param pctime [in]

Either the new creation time for the element or <b>NULL</b> if the creation time is not to be modified.


### -param patime [in]

Either the new access time for the element or <b>NULL</b> if the access time is not to be modified.


### -param pmtime [in]

Either the new modification time for the element or <b>NULL</b> if the modification time is not to be modified.


## -returns



This method can return one of these values.




## -remarks



<b>SetElementTimes</b>  sets time statistics for the specified storage element within this storage object.

Not all file systems support all the time values. This method sets those times that are supported and ignores the rest. Each time-value parameter can be <b>NULL</b>; indicating that no modification should occur.

Call the 
<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a> method to retrieve these time values.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>
 

 

