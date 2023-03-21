---
UID: NE:fsrmenums._FsrmGetFilePropertyOptions
title: FsrmGetFilePropertyOptions (fsrmenums.h)
description: Flags that defines how classification properties associated with a file are retrieved.
helpviewer_keywords: ["FsrmGetFilePropertyOptions","FsrmGetFilePropertyOptions enumeration [File Server Resource Manager]","FsrmGetFilePropertyOptions_FailOnPersistErrors","FsrmGetFilePropertyOptions_NoRuleEvaluation","FsrmGetFilePropertyOptions_None","FsrmGetFilePropertyOptions_Persistent","FsrmGetFilePropertyOptions_SkipOrphaned","fs.fsrmgetfilepropertyoptions","fsrm.fsrmgetfilepropertyoptions","fsrm/FsrmGetFilePropertyOptions","fsrm/FsrmGetFilePropertyOptions_FailOnPersistErrors","fsrm/FsrmGetFilePropertyOptions_NoRuleEvaluation","fsrm/FsrmGetFilePropertyOptions_None","fsrm/FsrmGetFilePropertyOptions_Persistent","fsrm/FsrmGetFilePropertyOptions_SkipOrphaned"]
old-location: fsrm\fsrmgetfilepropertyoptions.htm
tech.root: fsrm
ms.assetid: d909e244-344f-4da9-987c-de406c2dc359
ms.date: 12/05/2018
ms.keywords: FsrmGetFilePropertyOptions, FsrmGetFilePropertyOptions enumeration [File Server Resource Manager], FsrmGetFilePropertyOptions_FailOnPersistErrors, FsrmGetFilePropertyOptions_NoRuleEvaluation, FsrmGetFilePropertyOptions_None, FsrmGetFilePropertyOptions_Persistent, FsrmGetFilePropertyOptions_SkipOrphaned, fs.fsrmgetfilepropertyoptions, fsrm.fsrmgetfilepropertyoptions, fsrm/FsrmGetFilePropertyOptions, fsrm/FsrmGetFilePropertyOptions_FailOnPersistErrors, fsrm/FsrmGetFilePropertyOptions_NoRuleEvaluation, fsrm/FsrmGetFilePropertyOptions_None, fsrm/FsrmGetFilePropertyOptions_Persistent, fsrm/FsrmGetFilePropertyOptions_SkipOrphaned
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, Fsrmenums.h
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
req.typenames: FsrmGetFilePropertyOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmGetFilePropertyOptions
 - fsrmenums/_FsrmGetFilePropertyOptions
 - FsrmGetFilePropertyOptions
 - fsrmenums/FsrmGetFilePropertyOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fsrm.h
api_name:
 - FsrmGetFilePropertyOptions
---

# FsrmGetFilePropertyOptions enumeration


## -description

Flags that defines how classification properties associated with a file are retrieved.

## -enum-fields

### -field FsrmGetFilePropertyOptions_None:0

Retrieve the most up-to-date classification properties. Using this value may require more time than the 
      <b>FsrmGetFilePropertyOptions_NoRuleEvaluation</b> value.

### -field FsrmGetFilePropertyOptions_NoRuleEvaluation:0x1

Retrieve classification properties from cache or storage without using any rule evaluation.

### -field FsrmGetFilePropertyOptions_Persistent:0x2

After retrieving the classification properties (and possibly reclassifying the file in the process), store 
       the classification properties with the file.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.

### -field FsrmGetFilePropertyOptions_FailOnPersistErrors:0x4

If the <b>FsrmGetFilePropertyOptions_Persistent</b> flag is set but the properties were 
       unable to be stored with the file, return a failure for the operation. If this flag is clear the operation will 
       not fail even though the properties were not persisted with the file.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.

### -field FsrmGetFilePropertyOptions_SkipOrphaned:0x8

If the <b>FsrmGetFilePropertyOptions_Persistent</b> flag is set, skip any properties 
       stored with the file that are not also defined for the machine.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumfileproperties">IFsrmClassificationManager::EnumFileProperties</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getfileproperty">IFsrmClassificationManager::GetFileProperty</a>
