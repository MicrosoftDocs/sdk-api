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

# _FsrmPropertyConditionType enumeration


## -description


Defines the possible comparison operations that can be used to determine whether a property value of a 
    file meets a particular condition.


## -enum-fields




### -field FsrmPropertyConditionType_Unknown

The operator is unknown; do not use this value.


### -field FsrmPropertyConditionType_Equal

The property condition is met if the property value is equal to a specified value.


### -field FsrmPropertyConditionType_NotEqual

The property condition is met if the property value is not equal to a specified value.


### -field FsrmPropertyConditionType_GreaterThan

The property condition is met if the property value is greater than a specified value.


### -field FsrmPropertyConditionType_LessThan

The property condition is met if the property value is less than a specified value.


### -field FsrmPropertyConditionType_Contain

The property condition is met if the property value contains the specified value.


### -field FsrmPropertyConditionType_Exist

The property condition is met if the property value exists.


### -field FsrmPropertyConditionType_NotExist

The property condition is met if the property value does not exist.


### -field FsrmPropertyConditionType_StartWith

The property condition is met if the property value starts with the specified value.


### -field FsrmPropertyConditionType_EndWith

The property condition is met if the property value ends with the specified value.


### -field FsrmPropertyConditionType_ContainedIn

The property condition is met if the property value is contained in the specified value.


### -field FsrmPropertyConditionType_PrefixOf

The property condition is met if the property value is a prefix of the specified value.


### -field FsrmPropertyConditionType_SuffixOf

The property condition is met if the property value is a suffix of the specified value.


### -field FsrmPropertyConditionType_MatchesPattern

The property condition is met if the property value matches the specified pattern. The pattern format is a 
       semicolon-separated list of wildcard patterns. For example "*.exe;*.com"

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>



<a href="https://msdn.microsoft.com/b04b238b-55df-4467-809f-dbbc4ebd5595">IFsrmFileConditionProperty.Operator</a>



<a href="https://msdn.microsoft.com/2cec0753-20ec-4df4-9a74-c65bfed28070">IFsrmPropertyCondition.Type</a>
 

 

