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

# DSA_GetItemPtr function


## -description


<p class="CCE_Message">[<b>DSA_GetItemPtr</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Gets a pointer to an element from a dynamic structure array (DSA).


## -parameters




### -param hdsa

TBD


### -param i

TBD




#### - index [in]

Type: <b>int</b>

The index of the element to be retrieved (zero-based).


#### - pdsa [in]

Type: <b>HDSA</b>

A handle to the DSA containing the element.


## -returns



Returns a pointer to the specified element or <b>NULL</b> if the call fails.




## -remarks



Using the element pointer that this function returns, you can modify the data in that element directly. However, be aware that a subsequent insert or destroy operation could cause this pointer value to become invalid or to point to a different element.



