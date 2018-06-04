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

# DSA_DestroyCallback function


## -description


<p class="CCE_Message">[<b>DSA_DestroyCallback</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Iterates through a dynamic structure array (DSA), calling a specified callback function on each item. Upon reaching the end of the array, the DSA is freed.


## -parameters




### -param hdsa

TBD


### -param pfnCB [in]

Type: <b><a href="https://msdn.microsoft.com/2309ab9f-bf2e-413a-bf4f-b2782cd5af9e">PFNDSAENUMCALLBACK</a></b>

A callback function pointer. For the callback function prototype, see <a href="https://msdn.microsoft.com/2309ab9f-bf2e-413a-bf4f-b2782cd5af9e">PFNDSAENUMCALLBACK</a>.


### -param pData [in]

Type: <b>void*</b>


          A callback data pointer. This pointer is, in turn, passed as a parameter to <i>pfnCB</i>.
        


#### - pdsa [in]

Type: <b>HDSA</b>

A handle to a DSA to walk and destroy.


## -returns



This function does not return a value.



