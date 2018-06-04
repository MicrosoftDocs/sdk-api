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

# DSA_AppendItem macro


## -description


Appends a new item to the end of a dynamic structure array (DSA).


## -parameters




### -param hdsa

TBD


### -param pitem

TBD






#### - pItem [in]

A pointer to the item that is to be inserted.


#### - pdsa [in]

A handle to the DSA in which to insert the item.


## -remarks



<div class="alert"><b>Note</b>  This macro wraps the <a href="https://msdn.microsoft.com/e7bc2301-ff7b-4ca7-bad8-a323d44ad5ae">DSA_InsertItem</a> function.</div>
<div> </div>
The actual data pointed to by <i>pItem</i> is copied into the DSA. Subsequent actions performed on that item do not affect the original copy.



