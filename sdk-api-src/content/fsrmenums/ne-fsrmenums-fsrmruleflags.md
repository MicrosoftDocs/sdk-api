---
UID: NE:fsrmenums._FsrmRuleFlags
title: FsrmRuleFlags (fsrmenums.h)
description: Defines the possible states of a rule.
helpviewer_keywords: ["FsrmRuleFlags","FsrmRuleFlags enumeration [File Server Resource Manager]","FsrmRuleFlags_ClearAutomaticallyClassifiedProperty","FsrmRuleFlags_ClearManuallyClassifiedProperty","FsrmRuleFlags_Disabled","FsrmRuleFlags_Invalid","fs.fsrmruleflags","fsrm.fsrmruleflags","fsrmenums/FsrmRuleFlags","fsrmenums/FsrmRuleFlags_ClearAutomaticallyClassifiedProperty","fsrmenums/FsrmRuleFlags_ClearManuallyClassifiedProperty","fsrmenums/FsrmRuleFlags_Disabled","fsrmenums/FsrmRuleFlags_Invalid"]
old-location: fsrm\fsrmruleflags.htm
tech.root: fsrm
ms.assetid: 81150d1e-4ce9-4c8f-a4d5-77f7c8759e59
ms.date: 12/05/2018
ms.keywords: FsrmRuleFlags, FsrmRuleFlags enumeration [File Server Resource Manager], FsrmRuleFlags_ClearAutomaticallyClassifiedProperty, FsrmRuleFlags_ClearManuallyClassifiedProperty, FsrmRuleFlags_Disabled, FsrmRuleFlags_Invalid, fs.fsrmruleflags, fsrm.fsrmruleflags, fsrmenums/FsrmRuleFlags, fsrmenums/FsrmRuleFlags_ClearAutomaticallyClassifiedProperty, fsrmenums/FsrmRuleFlags_ClearManuallyClassifiedProperty, fsrmenums/FsrmRuleFlags_Disabled, fsrmenums/FsrmRuleFlags_Invalid
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FsrmRuleFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmRuleFlags
 - fsrmenums/_FsrmRuleFlags
 - FsrmRuleFlags
 - fsrmenums/FsrmRuleFlags
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
 - FsrmRuleFlags
---

# FsrmRuleFlags enumeration


## -description

Defines the possible states of a rule.

## -enum-fields

### -field FsrmRuleFlags_Disabled:0x100

Disable the rule; do not use the rule to classify files.

### -field FsrmRuleFlags_ClearAutomaticallyClassifiedProperty:0x400

Clear any automatically classified property referenced by this rule if the rule conditions are no longer met. 
       This can be useful if the file contents or metadata changed and the property previously assigned by automatic 
       classification no longer apply.

<b>Windows Server 2012 and Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012 R2.

### -field FsrmRuleFlags_ClearManuallyClassifiedProperty:0x800

Clear any manually classified property referenced by this rule if the rule conditions are no longer met. This 
       can be useful if the file contents or metadata changed and the property previously assigned by manual 
       classification no longer apply.

<b>Windows Server 2012 and Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012 R2.

### -field FsrmRuleFlags_Invalid:0x1000

Do not set this flag. FSRM sets this flag if the classifier that uses the rule is either disabled or not 
      registered with FSRM. If this flag is set FSRM will not use the rule to classify files.

## -remarks

You cannot set <b>FsrmRuleFlags_Invalid</b>; this flag is used by FSRM.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmrule-get_ruleflags">IFsrmRule.RuleFlags</a>
