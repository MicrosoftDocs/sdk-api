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

# MI_Context_GetCustomOptionAt function


## -description


Retrieves an option at a particular index that was set by the client.


## -parameters




### -param context [in]

A pointer to the request context.


### -param index [in]

The index of the option being retrieved. The index is zero based.


### -param name

A pointer to a pointer to the returned name or the retrieved option.


### -param valueType [out, optional]

A pointer to the returned option type. This parameter is optional.


### -param value [out, optional]

A pointer to the returned option value. This parameter is optional.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



Note that the index used does not relate to the order in which the client may have created the options.



