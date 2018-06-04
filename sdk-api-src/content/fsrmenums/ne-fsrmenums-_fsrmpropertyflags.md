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
 

 

