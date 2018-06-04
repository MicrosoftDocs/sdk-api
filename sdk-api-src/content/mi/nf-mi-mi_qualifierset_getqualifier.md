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

# MI_QualifierSet_GetQualifier function


## -description


Gets the qualifier information based on the given qualifier name.


## -parameters




### -param self [in]


<a href="https://msdn.microsoft.com/6c374d19-c433-4c70-a644-e53a401f96dd">MI_QualifierSet</a> structure.


### -param name

A null-terminated string that represents the name of the qualifier to get.


### -param qualifierType [out]

Returned qualifier type.


### -param qualifierFlags [out]

Returned qualifier flags that indicate the scope of a qualifier.


### -param qualifierValue [out]

Returned qualifier value. This value has the lifetime of the qualifier set.


### -param index [out]

Returned zero-based index of the qualifier.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



