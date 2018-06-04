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

# _FsrmPropertyValueType enumeration


## -description


Enumerates the type of the value being assigned to an FSRM property in a property 
    condition.


## -enum-fields




### -field FsrmPropertyValueType_Undefined

The type assigned to the property value is not defined.


### -field FsrmPropertyValueType_Literal

The type assigned to the property value is one or more literal values.


### -field FsrmPropertyValueType_DateOffset

The type assigned to the property value is a date expression containing a date variable and an optional 
      date offset.


## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>



<a href="https://msdn.microsoft.com/86086089-936a-428f-bc2b-514c873db1a3">IFsrmFileConditionProperty.ValueType</a>
 

 

