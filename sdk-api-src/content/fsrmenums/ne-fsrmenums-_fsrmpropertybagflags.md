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
 

 

