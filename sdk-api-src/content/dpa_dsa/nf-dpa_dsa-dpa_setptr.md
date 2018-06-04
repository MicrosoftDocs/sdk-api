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

# DPA_SetPtr function


## -description


<p class="CCE_Message">[<b>DPA_SetPtr</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Assigns a value to an item in a dynamic pointer array (DPA).


## -parameters




### -param hdpa

TBD


### -param i

TBD


### -param p

Type: <b>void*</b>

A pointer to the value to assign to the specified DPA item.


#### - index

Type: <b>int</b>

The index of the item in the DPA. 

<div class="alert"><b>Note</b>  If the index is beyond the current size of the DPA, the DPA expands to accommodate it. You do not need to assign items contiguously.</div>
<div> </div>

#### - pdpa

Type: <b>HDPA</b>

A handle to a DPA.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.



