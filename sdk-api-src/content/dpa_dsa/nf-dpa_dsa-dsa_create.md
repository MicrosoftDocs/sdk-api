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

# DSA_Create function


## -description


<p class="CCE_Message">[<b>DSA_Create</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Creates a dynamic structure array (DSA).


## -parameters




### -param cbItem [in]

Type: <b>int</b>

The size, in bytes, of the item.


### -param cItemGrow

TBD




#### - cbItemGrow [in]

Type: <b>int</b>

The number of items by which the array should be incremented, if the DSA needs to be enlarged.


## -returns



Type: <b>HDSA</b>

Returns a handle to a DSA if successful, or <b>NULL</b> if the creation fails.




## -remarks



Unlike a dynamic pointer array (DPA), a DSA can contain elements of any size. This allows structures to be stored directly in the array.



