---
UID: NE:fsrmenums._FsrmRuleType
title: FsrmRuleType (fsrmenums.h)
author: windows-sdk-content
description: Defines the types of rules that you can define.
old-location: fsrm\fsrmruletype.htm
tech.root: fsrm
ms.assetid: 9fd9daf2-5e3e-4d9c-8f19-92e31756a1c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmRuleType, FsrmRuleType enumeration [File Server Resource Manager], FsrmRuleType_Classification, FsrmRuleType_Generic, FsrmRuleType_Unknown, fs.fsrmruletype, fsrm.fsrmruletype, fsrmenums/FsrmRuleType, fsrmenums/FsrmRuleType_Classification, fsrmenums/FsrmRuleType_Generic, fsrmenums/FsrmRuleType_Unknown
ms.topic: enum
f1_keywords: 
 - "fsrmenums/FsrmRuleType"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmRuleType
targetos: Windows
req.typenames: FsrmRuleType
req.redist: 
ms.custom: 19H1
---

# FsrmRuleType enumeration


## -description


Defines the types of rules that you can define.


## -enum-fields




### -field FsrmRuleType_Unknown

The rule is unknown. Do not use this type.


### -field FsrmRuleType_Classification

The rule defines how a classification module affects a file.


### -field FsrmRuleType_Generic

For internal use only.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createrule">IFsrmClassificationManager::CreateRule</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumrules">IFsrmClassificationManager::EnumRules</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getrule">IFsrmClassificationManager::GetRule</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmrule-get_ruletype">IFsrmRule.RuleType</a>
 

 

