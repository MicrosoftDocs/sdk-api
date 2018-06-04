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

# DSA_InsertItem function


## -description


<p class="CCE_Message">[<b>DSA_InsertItem</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Inserts a new item into a dynamic structure array (DSA). If necessary, the DSA expands to accommodate the new item.


## -parameters




### -param hdsa

TBD


### -param i

TBD


### -param pitem

TBD




#### - index [in]

Type: <b>int</b>

The position in the DSA where new item is to be inserted, or DSA_APPEND to insert the item at the end of the array.


#### - pItem [in]

Type: <b>void*</b>

A pointer to the item that is to be inserted.


#### - pdsa [in]

Type: <b>HDSA</b>

A handle to the DSA in which to insert the item.


## -returns



Type: <b>int</b>

Returns the index of the new item if the insertion succeeds, or DSA_ERR (<code>-1</code>) if the insertion fails.




## -remarks



The actual data pointed to by <i>pItem</i> is copied into the DSA. Subsequent actions performed on that item do not affect the original copy.



