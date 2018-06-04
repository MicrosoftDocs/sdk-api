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

# DSA_EnumCallback function


## -description


Iterates through the  dynamic structure array (DSA) and calls <i>pfnCB</i> on each item. 


## -parameters




### -param hdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.


### -param pfnCB [in]

Type: <b><a href="https://msdn.microsoft.com/d5146b5b-1a1c-4584-ba2f-de7f8db654cb">PFNDAENUMCALLBACK</a>*</b>

A callback function pointer. See <a href="https://msdn.microsoft.com/2309ab9f-bf2e-413a-bf4f-b2782cd5af9e">PFNDSAENUMCALLBACK</a> for the callback function prototype.


### -param pData [in]

Type: <b>void*</b>

A callback data pointer. <i>pData</i> is passed as a parameter to <i>pfnCB</i>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/2fe1546f-d517-4d63-a3a6-1d3ea0238b3d">PFNDAENUMCALLBACKCONST</a>
 

 

