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

# _FsrmRuleFlags enumeration


## -description


Defines the possible states of a rule.


## -enum-fields




### -field FsrmRuleFlags_Disabled

Disable the rule; do not use the rule to classify files.


### -field FsrmRuleFlags_ClearAutomaticallyClassifiedProperty

Clear any automatically classified property referenced by this rule if the rule conditions are no longer met. 
       This can be useful if the file contents or metadata changed and the property previously assigned by automatic 
       classification no longer apply.

<b>Windows Server 2012 and Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012 R2.


### -field FsrmRuleFlags_ClearManuallyClassifiedProperty

Clear any manually classified property referenced by this rule if the rule conditions are no longer met. This 
       can be useful if the file contents or metadata changed and the property previously assigned by manual 
       classification no longer apply.

<b>Windows Server 2012 and Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012 R2.


### -field FsrmRuleFlags_Invalid

Do not set this flag. FSRM sets this flag if the classifier that uses the rule is either disabled or not 
      registered with FSRM. If this flag is set FSRM will not use the rule to classify files.


## -remarks



You cannot set <b>FsrmRuleFlags_Invalid</b>; this flag is used by FSRM.




## -see-also




<a href="https://msdn.microsoft.com/c656115a-a0d4-4860-9756-98df84c1672f">IFsrmRule.RuleFlags</a>
 

 

