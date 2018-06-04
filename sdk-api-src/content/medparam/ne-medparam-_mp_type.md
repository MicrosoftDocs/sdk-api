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

# _MP_Type enumeration


## -description



The <code>MP_TYPE</code> enumeration specifies the data type for a parameter.




## -enum-fields




### -field MPT_INT

Value is a signed 32-bit integer.


### -field MPT_FLOAT

Value is a 32-bit IEEE floating-point value.


### -field MPT_BOOL

Value is Boolean. Use the following constants for Boolean parameters:


### -field MPT_ENUM

Value is taken from a set of consecutive integers.


### -field MPT_MAX

Reserved.


## -remarks



To reduce type conversions at run time, all parameters have 32-bit float values, defined as type <b>MP_DATA</b>. The members of this enumeration specify how a given parameter should be interpreted.




## -see-also




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/91d2d08b-a55e-492f-a509-9c080cc438df">MP_PARAMINFO</a>
 

 

