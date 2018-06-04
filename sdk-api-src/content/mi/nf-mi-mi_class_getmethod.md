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

# MI_Class_GetMethod function


## -description


Gets details of a method based on the method name.


## -parameters




### -param self [in]

A pointer to the class object from which the method information is to be retrieved.


### -param name [in]

The name of the method to be retrieved.


### -param qualifierSet [out, optional]

A pointer to the variable to receive the returned method qualifier set.   This parameter is optional. The memory associated with the qualifier set is valid until the class object is deleted. When you have finished using the class qualifier set, delete the class object by calling the <a href="https://msdn.microsoft.com/a2794f8f-a69a-49f3-8d7e-512c80ea782b">MI_Class_Delete</a> function. If this information is not needed, pass <b>NULL</b> for this parameter.


### -param parameterSet [out, optional]

A pointer to a variable to receive the returned parameter set. The parameter set also contains the return type and return type qualifier set.   This parameter is optional. The memory associated with the parameter set is valid until the class object is deleted. When you have finished using the parameter set, delete the class object by calling the <a href="https://msdn.microsoft.com/a2794f8f-a69a-49f3-8d7e-512c80ea782b">MI_Class_Delete</a> function. If this information is not needed, pass <b>NULL</b> for this parameter.


### -param index [out, optional]

A pointer to a variable to receive the returned index of the specified method. This parameter is optional.


## -returns



This function returns MI_INLINE MI_Result.



