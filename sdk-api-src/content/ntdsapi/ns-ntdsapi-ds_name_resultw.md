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

# DS_NAME_RESULTW structure


## -description


The <b>DS_NAME_RESULT</b> structure is used with the <a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a> function to contain the  names converted by the function.


## -struct-fields




### -field cItems

Contains the number of elements in the <b>rItems</b> array.


### -field rItems.size_is

 


### -field rItems.size_is.cItems

 


### -field rItems

Contains an array of <a href="https://msdn.microsoft.com/50a4488f-e2d4-4671-b0e7-fb8cb4096c5c">DS_NAME_RESULT_ITEM</a> structure pointers. Each element of this array represents a single converted name.


## -see-also




<a href="https://msdn.microsoft.com/50a4488f-e2d4-4671-b0e7-fb8cb4096c5c">DS_NAME_RESULT_ITEM</a>



<a href="https://msdn.microsoft.com/42b20d3b-1799-4f5f-b74e-fe9284dd8ac3">Domain Controller and Replication Management Structures</a>



<a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a>
 

 

