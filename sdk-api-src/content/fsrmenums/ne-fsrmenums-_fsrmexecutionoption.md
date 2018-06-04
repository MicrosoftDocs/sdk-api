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

# _FsrmExecutionOption enumeration


## -description


Defines the options for how to apply the rule to the file.


## -enum-fields




### -field FsrmExecutionOption_Unknown

The execution option is unknown. Do not use this value.


### -field FsrmExecutionOption_EvaluateUnset

The rule is applied as a default value to the file if the property is not set on the file (if none of the 
      storage modules returns the property).


### -field FsrmExecutionOption_ReEvaluate_ConsiderExistingValue

The rule is applied to the file considering default and existing values using aggregation rules (for 
      aggregation rules, see 
      <a href="https://msdn.microsoft.com/618335a2-2b37-43e2-adaa-2a6d06464627">FsrmPropertyDefinitionType</a>).


### -field FsrmExecutionOption_ReEvaluate_IgnoreExistingValue

The rule is applied to the file but  default and existing values are ignored.


## -see-also




<a href="https://msdn.microsoft.com/e084c056-18b1-4089-bab9-fce2ef58cd05">IFsrmClassificationRule.ExecutionOption</a>
 

 

