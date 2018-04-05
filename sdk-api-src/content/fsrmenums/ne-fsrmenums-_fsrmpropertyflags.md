---
UID: NE:fsrmenums._FsrmPropertyFlags
title: "_FsrmPropertyFlags"
author: windows-driver-content
description: Defines flag values that provide additional information about a classification property.
old-location: fsrm\fsrmpropertyflags.htm
old-project: Fsrm
ms.assetid: f5ce3ed3-5a3d-4ef5-9f67-0f19f21e41aa
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: FsrmPropertyFlags, FsrmPropertyFlags enumeration [File Server Resource Manager], FsrmPropertyFlags_AggregationFailed, FsrmPropertyFlags_Deleted, FsrmPropertyFlags_Existing, FsrmPropertyFlags_ExplicitValueDeleted, FsrmPropertyFlags_FailedClassifyingProperties, FsrmPropertyFlags_FailedLoadingProperties, FsrmPropertyFlags_FailedSavingProperties, FsrmPropertyFlags_Inherited, FsrmPropertyFlags_Manual, FsrmPropertyFlags_Orphaned, FsrmPropertyFlags_PersistentMask, FsrmPropertyFlags_PolicyDerived, FsrmPropertyFlags_PropertyDeletedFromClear, FsrmPropertyFlags_PropertySourceMask, FsrmPropertyFlags_Reclassified, FsrmPropertyFlags_RetrievedFromCache, FsrmPropertyFlags_RetrievedFromStorage, FsrmPropertyFlags_Secure, FsrmPropertyFlags_SetByClassifier, _FsrmPropertyFlags, fs.fsrmpropertyflags, fsrm.fsrmpropertyflags, fsrmenums/FsrmPropertyFlags, fsrmenums/FsrmPropertyFlags_AggregationFailed, fsrmenums/FsrmPropertyFlags_Deleted, fsrmenums/FsrmPropertyFlags_Existing, fsrmenums/FsrmPropertyFlags_ExplicitValueDeleted, fsrmenums/FsrmPropertyFlags_FailedClassifyingProperties, fsrmenums/FsrmPropertyFlags_FailedLoadingProperties, fsrmenums/FsrmPropertyFlags_FailedSavingProperties, fsrmenums/FsrmPropertyFlags_Inherited, fsrmenums/FsrmPropertyFlags_Manual, fsrmenums/FsrmPropertyFlags_Orphaned, fsrmenums/FsrmPropertyFlags_PersistentMask, fsrmenums/FsrmPropertyFlags_PolicyDerived, fsrmenums/FsrmPropertyFlags_PropertyDeletedFromClear, fsrmenums/FsrmPropertyFlags_PropertySourceMask, fsrmenums/FsrmPropertyFlags_Reclassified, fsrmenums/FsrmPropertyFlags_RetrievedFromCache, fsrmenums/FsrmPropertyFlags_RetrievedFromStorage, fsrmenums/FsrmPropertyFlags_Secure, fsrmenums/FsrmPropertyFlags_SetByClassifier
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
req.typenames: FsrmPropertyFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	FsrmEnums.h
api_name:
-	FsrmPropertyFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# _FsrmPropertyFlags enumeration


## -description


Defines flag values that provide additional information about a classification property.


## -enum-fields




### -field FsrmPropertyFlags_None


### -field FsrmPropertyFlags_Orphaned

The property does not have a corresponding property definition defined in FSRM.


### -field FsrmPropertyFlags_RetrievedFromCache

The value of the property was retrieved from the cache during this classification session.


### -field FsrmPropertyFlags_RetrievedFromStorage

The value of the property was retrieved from the file or database during this classification session.


### -field FsrmPropertyFlags_SetByClassifier

The value of the property was set by a classification rule during the last classification run.


### -field FsrmPropertyFlags_Deleted

The property was deleted by 
      <a href="https://msdn.microsoft.com/bac42416-0757-462f-8869-339655f48587">IFsrmClassificationManager::ClearFileProperty</a>.


### -field FsrmPropertyFlags_Reclassified

The property value from storage was changed to a different value by a classifier.


### -field FsrmPropertyFlags_AggregationFailed

There are values from multiple sources that could not be aggregated together.


### -field FsrmPropertyFlags_Existing

The property already exists in storage.


### -field FsrmPropertyFlags_FailedLoadingProperties

The property may only be partially classified because a failure occurred while loading properties from 
      storage.


### -field FsrmPropertyFlags_FailedClassifyingProperties

The property may only be partially classified because a failure occurred while classifying 
      properties.


### -field FsrmPropertyFlags_FailedSavingProperties

The property failed to be saved by the storage module with the highest precedence.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


### -field FsrmPropertyFlags_Secure

The property is defined to be used for security purposes or came from secure storage.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


### -field FsrmPropertyFlags_PolicyDerived

The property value originally came from a classification policy.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


### -field FsrmPropertyFlags_Inherited

The property value was inherited from the property value of the file's parent folder.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


### -field FsrmPropertyFlags_Manual

The property value was set manually.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


### -field FsrmPropertyFlags_ExplicitValueDeleted

An explicit property value was deleted and replaced with an inherited value.

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


### -field FsrmPropertyFlags_PropertyDeletedFromClear

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




<a href="https://msdn.microsoft.com/59c52ac2-82ef-4dfa-85e9-450149c2e904">IFsrmProperty.PropertyFlags</a>
 

 

