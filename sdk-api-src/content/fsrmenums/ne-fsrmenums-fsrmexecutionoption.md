---
UID: NE:fsrmenums._FsrmExecutionOption
title: FsrmExecutionOption (fsrmenums.h)
description: Defines the options for how to apply the rule to the file.
helpviewer_keywords: ["FsrmExecutionOption","FsrmExecutionOption enumeration [File Server Resource Manager]","FsrmExecutionOption_EvaluateUnset","FsrmExecutionOption_ReEvaluate_ConsiderExistingValue","FsrmExecutionOption_ReEvaluate_IgnoreExistingValue","FsrmExecutionOption_Unknown","fs.fsrmexecutionoption","fsrm.fsrmexecutionoption","fsrmenums/FsrmExecutionOption","fsrmenums/FsrmExecutionOption_EvaluateUnset","fsrmenums/FsrmExecutionOption_ReEvaluate_ConsiderExistingValue","fsrmenums/FsrmExecutionOption_ReEvaluate_IgnoreExistingValue","fsrmenums/FsrmExecutionOption_Unknown"]
old-location: fsrm\fsrmexecutionoption.htm
tech.root: fsrm
ms.assetid: 55512fe2-0249-4c6f-90bf-5f769674bedd
ms.date: 12/05/2018
ms.keywords: FsrmExecutionOption, FsrmExecutionOption enumeration [File Server Resource Manager], FsrmExecutionOption_EvaluateUnset, FsrmExecutionOption_ReEvaluate_ConsiderExistingValue, FsrmExecutionOption_ReEvaluate_IgnoreExistingValue, FsrmExecutionOption_Unknown, fs.fsrmexecutionoption, fsrm.fsrmexecutionoption, fsrmenums/FsrmExecutionOption, fsrmenums/FsrmExecutionOption_EvaluateUnset, fsrmenums/FsrmExecutionOption_ReEvaluate_ConsiderExistingValue, fsrmenums/FsrmExecutionOption_ReEvaluate_IgnoreExistingValue, fsrmenums/FsrmExecutionOption_Unknown
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FsrmExecutionOption
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmExecutionOption
 - fsrmenums/_FsrmExecutionOption
 - FsrmExecutionOption
 - fsrmenums/FsrmExecutionOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmExecutionOption
---

# FsrmExecutionOption enumeration


## -description

Defines the options for how to apply the rule to the file.

## -enum-fields

### -field FsrmExecutionOption_Unknown:0

The execution option is unknown. Do not use this value.

### -field FsrmExecutionOption_EvaluateUnset:1

The rule is applied as a default value to the file if the property is not set on the file (if none of the 
      storage modules returns the property).

### -field FsrmExecutionOption_ReEvaluate_ConsiderExistingValue:2

The rule is applied to the file considering default and existing values using aggregation rules (for 
      aggregation rules, see 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpropertydefinitiontype">FsrmPropertyDefinitionType</a>).

### -field FsrmExecutionOption_ReEvaluate_IgnoreExistingValue:3

The rule is applied to the file but  default and existing values are ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationrule-get_executionoption">IFsrmClassificationRule.ExecutionOption</a>
