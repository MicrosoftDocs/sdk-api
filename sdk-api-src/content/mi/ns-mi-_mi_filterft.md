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

# _MI_FilterFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/0849cb55-ba2f-4855-ac33-fa96d8ecd94f">MI_Filter</a> 
    structure. Use the functions with the name prefix "MI_Filter_" to manipulate these 
    structures.


## -struct-fields






#### - Evaluate

The provider calls this function to evaluate an instance against a given filter. See 
       <a href="https://msdn.microsoft.com/b826f02d-3764-4f61-996f-42bf01ea44e2">MI_Filter_Evaluate</a>.


#### - GetExpression

Gets the filter language and expression. See 
       <a href="https://msdn.microsoft.com/a1ba9cf2-b613-4621-a4ac-39808b4bfd8e">MI_Filter_GetExpression</a>.

