---
UID: NE:fsrmenums._FsrmRuleType
title: "_FsrmRuleType"
author: windows-sdk-content
description: Defines the types of rules that you can define.
old-location: fsrm\fsrmruletype.htm
old-project: Fsrm
ms.assetid: 9fd9daf2-5e3e-4d9c-8f19-92e31756a1c7
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FsrmRuleType, FsrmRuleType enumeration [File Server Resource Manager], FsrmRuleType_Classification, FsrmRuleType_Generic, FsrmRuleType_Unknown, _FsrmRuleType, fs.fsrmruletype, fsrm.fsrmruletype, fsrmenums/FsrmRuleType, fsrmenums/FsrmRuleType_Classification, fsrmenums/FsrmRuleType_Generic, fsrmenums/FsrmRuleType_Unknown
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmRuleType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmRuleType
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# _FsrmRuleType enumeration


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




<a href="https://msdn.microsoft.com/ca9a97b7-eadd-4f57-8f3a-afa439222f21">IFsrmClassificationManager::CreateRule</a>



<a href="https://msdn.microsoft.com/2f67527c-cde3-4907-9e61-4d9e18b18859">IFsrmClassificationManager::EnumRules</a>



<a href="https://msdn.microsoft.com/2c21ed09-6c69-4f03-91bb-9beeb816ed62">IFsrmClassificationManager::GetRule</a>



<a href="https://msdn.microsoft.com/a1aa2c94-b2f0-4620-8589-27360f5bdf05">IFsrmRule.RuleType</a>
 

 

