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

# _MI_ParameterSetFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/14b5773c-4741-453b-824a-226aab9b8a10">MI_ParameterSet</a> structure.  Use the functions with the name prefix MI_ParameterSet_ to manipulate these structures.


## -struct-fields






#### - GetMethodReturnType

Gets the method return type and qualifier set for a specified parameter set. See <a href="https://msdn.microsoft.com/8d2e881a-72a8-4819-a407-b7381ab7a94a">MI_ParameterSet_GetMethodReturnType</a>.


#### - GetParameter

Gets a method's parameter information based on a parameter name. See <a href="https://msdn.microsoft.com/ff895beb-8354-488d-9c97-2d0448da954a">MI_ParameterSet_GetParameter</a>.


#### - GetParameterAt

Gets a method's parameter information at the specified index. See <a href="https://msdn.microsoft.com/fcfd7104-dd63-4a48-9a20-dcec0dc33242">MI_ParameterSet_GetParameterAt</a>.


#### - GetParameterCount

Gets the number of parameters in a parameter set. See <a href="https://msdn.microsoft.com/4b1ca06f-426c-483f-a571-b49eb06991e1">MI_ParameterSet_GetParameterCount</a>.

