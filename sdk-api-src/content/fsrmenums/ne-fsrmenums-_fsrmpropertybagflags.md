---
UID: NE:fsrmenums._FsrmPropertyBagFlags
title: "_FsrmPropertyBagFlags"
author: windows-sdk-content
description: Defines flag values that provide additional information about the property bag.
old-location: fsrm\fsrmpropertybagflags.htm
tech.root: Fsrm
ms.assetid: 5b434ab6-4c15-4960-b5d1-c90da806e9d8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FsrmPropertyBagFlags, FsrmPropertyBagFlags enumeration [File Server Resource Manager], FsrmPropertyBagFlags_FailedClassifyingProperties, FsrmPropertyBagFlags_FailedLoadingProperties, FsrmPropertyBagFlags_FailedSavingProperties, FsrmPropertyBagFlags_UpdatedByClassifier, _FsrmPropertyBagFlags, fs.fsrmpropertybagflags, fsrm.fsrmpropertybagflags, fsrmenums/FsrmPropertyBagFlags, fsrmenums/FsrmPropertyBagFlags_FailedClassifyingProperties, fsrmenums/FsrmPropertyBagFlags_FailedLoadingProperties, fsrmenums/FsrmPropertyBagFlags_FailedSavingProperties, fsrmenums/FsrmPropertyBagFlags_UpdatedByClassifier
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
 - FsrmPropertyBagFlags
product: Windows
targetos: Windows
req.typenames: FsrmPropertyBagFlags
req.redist: 
---

# _FsrmPropertyBagFlags enumeration


## -description


Defines flag values that provide additional information about the property bag.


## -enum-fields




### -field FsrmPropertyBagFlags_UpdatedByClassifier

The properties in the property bag were updated by a classifier.


### -field FsrmPropertyBagFlags_FailedLoadingProperties

The properties in the property bag may only be partially classified because a failure occurred while loading properties from storage.


### -field FsrmPropertyBagFlags_FailedSavingProperties

The properties in the property bag failed to be saved by the storage module with the highest precedence.


### -field FsrmPropertyBagFlags_FailedClassifyingProperties

The properties in the property bag may only be partially classified because a failure occurred while classifying properties.


## -see-also




<a href="https://msdn.microsoft.com/b7e5885e-c716-4fa8-afc0-bfe258e5f421">IFsrmPropertyBag::PropertyBagFlags</a>
 

 

