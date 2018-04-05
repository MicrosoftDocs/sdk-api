---
UID: NE:fsrmenums._FsrmExecutionOption
title: "_FsrmExecutionOption"
author: windows-driver-content
description: Defines the options for how to apply the rule to the file.
old-location: fsrm\fsrmexecutionoption.htm
old-project: Fsrm
ms.assetid: 55512fe2-0249-4c6f-90bf-5f769674bedd
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: FsrmExecutionOption, FsrmExecutionOption enumeration [File Server Resource Manager], FsrmExecutionOption_EvaluateUnset, FsrmExecutionOption_ReEvaluate_ConsiderExistingValue, FsrmExecutionOption_ReEvaluate_IgnoreExistingValue, FsrmExecutionOption_Unknown, _FsrmExecutionOption, fs.fsrmexecutionoption, fsrm.fsrmexecutionoption, fsrmenums/FsrmExecutionOption, fsrmenums/FsrmExecutionOption_EvaluateUnset, fsrmenums/FsrmExecutionOption_ReEvaluate_ConsiderExistingValue, fsrmenums/FsrmExecutionOption_ReEvaluate_IgnoreExistingValue, fsrmenums/FsrmExecutionOption_Unknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmEnums.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FsrmExecutionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	FsrmEnums.h
api_name:
-	FsrmExecutionOption
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
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
 

 

