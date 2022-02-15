---
UID: NE:fsrmenums._FsrmPropertyFlags
title: FsrmPropertyFlags (fsrmenums.h)
description: Defines flag values that provide additional information about a classification property.
helpviewer_keywords: ["FsrmPropertyFlags","FsrmPropertyFlags enumeration [File Server Resource Manager]","FsrmPropertyFlags_AggregationFailed","FsrmPropertyFlags_Deleted","FsrmPropertyFlags_Existing","FsrmPropertyFlags_ExplicitValueDeleted","FsrmPropertyFlags_FailedClassifyingProperties","FsrmPropertyFlags_FailedLoadingProperties","FsrmPropertyFlags_FailedSavingProperties","FsrmPropertyFlags_Inherited","FsrmPropertyFlags_Manual","FsrmPropertyFlags_Orphaned","FsrmPropertyFlags_PersistentMask","FsrmPropertyFlags_PolicyDerived","FsrmPropertyFlags_PropertyDeletedFromClear","FsrmPropertyFlags_PropertySourceMask","FsrmPropertyFlags_Reclassified","FsrmPropertyFlags_RetrievedFromCache","FsrmPropertyFlags_RetrievedFromStorage","FsrmPropertyFlags_Secure","FsrmPropertyFlags_SetByClassifier","fs.fsrmpropertyflags","fsrm.fsrmpropertyflags","fsrmenums/FsrmPropertyFlags","fsrmenums/FsrmPropertyFlags_AggregationFailed","fsrmenums/FsrmPropertyFlags_Deleted","fsrmenums/FsrmPropertyFlags_Existing","fsrmenums/FsrmPropertyFlags_ExplicitValueDeleted","fsrmenums/FsrmPropertyFlags_FailedClassifyingProperties","fsrmenums/FsrmPropertyFlags_FailedLoadingProperties","fsrmenums/FsrmPropertyFlags_FailedSavingProperties","fsrmenums/FsrmPropertyFlags_Inherited","fsrmenums/FsrmPropertyFlags_Manual","fsrmenums/FsrmPropertyFlags_Orphaned","fsrmenums/FsrmPropertyFlags_PersistentMask","fsrmenums/FsrmPropertyFlags_PolicyDerived","fsrmenums/FsrmPropertyFlags_PropertyDeletedFromClear","fsrmenums/FsrmPropertyFlags_PropertySourceMask","fsrmenums/FsrmPropertyFlags_Reclassified","fsrmenums/FsrmPropertyFlags_RetrievedFromCache","fsrmenums/FsrmPropertyFlags_RetrievedFromStorage","fsrmenums/FsrmPropertyFlags_Secure","fsrmenums/FsrmPropertyFlags_SetByClassifier"]
old-location: fsrm\fsrmpropertyflags.htm
tech.root: fsrm
ms.assetid: f5ce3ed3-5a3d-4ef5-9f67-0f19f21e41aa
ms.date: 12/05/2018
ms.keywords: FsrmPropertyFlags, FsrmPropertyFlags enumeration [File Server Resource Manager], FsrmPropertyFlags_AggregationFailed, FsrmPropertyFlags_Deleted, FsrmPropertyFlags_Existing, FsrmPropertyFlags_ExplicitValueDeleted, FsrmPropertyFlags_FailedClassifyingProperties, FsrmPropertyFlags_FailedLoadingProperties, FsrmPropertyFlags_FailedSavingProperties, FsrmPropertyFlags_Inherited, FsrmPropertyFlags_Manual, FsrmPropertyFlags_Orphaned, FsrmPropertyFlags_PersistentMask, FsrmPropertyFlags_PolicyDerived, FsrmPropertyFlags_PropertyDeletedFromClear, FsrmPropertyFlags_PropertySourceMask, FsrmPropertyFlags_Reclassified, FsrmPropertyFlags_RetrievedFromCache, FsrmPropertyFlags_RetrievedFromStorage, FsrmPropertyFlags_Secure, FsrmPropertyFlags_SetByClassifier, fs.fsrmpropertyflags, fsrm.fsrmpropertyflags, fsrmenums/FsrmPropertyFlags, fsrmenums/FsrmPropertyFlags_AggregationFailed, fsrmenums/FsrmPropertyFlags_Deleted, fsrmenums/FsrmPropertyFlags_Existing, fsrmenums/FsrmPropertyFlags_ExplicitValueDeleted, fsrmenums/FsrmPropertyFlags_FailedClassifyingProperties, fsrmenums/FsrmPropertyFlags_FailedLoadingProperties, fsrmenums/FsrmPropertyFlags_FailedSavingProperties, fsrmenums/FsrmPropertyFlags_Inherited, fsrmenums/FsrmPropertyFlags_Manual, fsrmenums/FsrmPropertyFlags_Orphaned, fsrmenums/FsrmPropertyFlags_PersistentMask, fsrmenums/FsrmPropertyFlags_PolicyDerived, fsrmenums/FsrmPropertyFlags_PropertyDeletedFromClear, fsrmenums/FsrmPropertyFlags_PropertySourceMask, fsrmenums/FsrmPropertyFlags_Reclassified, fsrmenums/FsrmPropertyFlags_RetrievedFromCache, fsrmenums/FsrmPropertyFlags_RetrievedFromStorage, fsrmenums/FsrmPropertyFlags_Secure, fsrmenums/FsrmPropertyFlags_SetByClassifier
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
req.typenames: FsrmPropertyFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmPropertyFlags
 - fsrmenums/_FsrmPropertyFlags
 - FsrmPropertyFlags
 - fsrmenums/FsrmPropertyFlags
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
 - FsrmPropertyFlags
---

# FsrmPropertyFlags enumeration


## -description

Defines flag values that provide additional information about a classification property.

## -enum-fields

### -field FsrmPropertyFlags_None:0

### -field FsrmPropertyFlags_Orphaned:0x1

The property does not have a corresponding property definition defined in FSRM.

### -field FsrmPropertyFlags_RetrievedFromCache:0x2

The value of the property was retrieved from the cache during this classification session.

### -field FsrmPropertyFlags_RetrievedFromStorage:0x4

The value of the property was retrieved from the file or database during this classification session.

### -field FsrmPropertyFlags_SetByClassifier:0x8

The value of the property was set by a classification rule during the last classification run.

### -field FsrmPropertyFlags_Deleted:0x10

The property was deleted by 
      <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-clearfileproperty">IFsrmClassificationManager::ClearFileProperty</a>.

### -field FsrmPropertyFlags_Reclassified:0x20

The property value from storage was changed to a different value by a classifier.

### -field FsrmPropertyFlags_AggregationFailed:0x40

There are values from multiple sources that could not be aggregated together.

### -field FsrmPropertyFlags_Existing:0x80

The property already exists in storage.

### -field FsrmPropertyFlags_FailedLoadingProperties:0x100

The property may only be partially classified because a failure occurred while loading properties from 
      storage.

### -field FsrmPropertyFlags_FailedClassifyingProperties:0x200

The property may only be partially classified because a failure occurred while classifying 
      properties.

### -field FsrmPropertyFlags_FailedSavingProperties:0x400

The property failed to be saved by the storage module with the highest precedence.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.

### -field FsrmPropertyFlags_Secure:0x800

The property is defined to be used for security purposes or came from secure storage.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.

### -field FsrmPropertyFlags_PolicyDerived:0x1000

The property value originally came from a classification policy.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.

### -field FsrmPropertyFlags_Inherited:0x2000

The property value was inherited from the property value of the file's parent folder.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.

### -field FsrmPropertyFlags_Manual:0x4000

The property value was set manually.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.

### -field FsrmPropertyFlags_ExplicitValueDeleted:0x8000

An explicit property value was deleted and replaced with an inherited value.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.

### -field FsrmPropertyFlags_PropertyDeletedFromClear:0x10000

The property has been deleted due to a rule marked with clear property.

<b>Windows Server 2012 and Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012 R2.

### -field FsrmPropertyFlags_PropertySourceMask

This mask shows which flags are used to indicate the source of the property and is equivalent to the 
       following flag combination:

<code>(FsrmPropertyFlags_RetrievedFromCache | FsrmPropertyFlags_RetrievedFromStorage | FsrmPropertyFlags_SetByClassifier)</code>

### -field FsrmPropertyFlags_PersistentMask

This mask shows which flags are persisted by the cache and secure storage modules and is equivalent to the 
       following flag combination:

<code>(FsrmPropertyFlags_PolicyDerived | FsrmPropertyFlags_Manual)</code>

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.

## -remarks

The <b>FsrmPropertyFlags_SetByClassifier</b> flag is set in the following cases:

<ul>
<li>This is the first time the property value is being applied.</li>
<li>The execution option of the classification rule applying the value is set to 
      <b>FsrmExecutionOption_ReEvaluate_IgnoreExistingValue</b>.</li>
<li>The execution option of the classification rule applying the value is set to 
      <b>FsrmExecutionOption_ReEvaluate_ConsiderExistingValue</b> and the aggregation policy set 
      the value specified by the rule.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmproperty-get_propertyflags">IFsrmProperty.PropertyFlags</a>
