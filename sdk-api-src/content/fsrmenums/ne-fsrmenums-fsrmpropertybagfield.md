---
UID: NE:fsrmenums._FsrmPropertyBagField
title: FsrmPropertyBagField (fsrmenums.h)
author: windows-sdk-content
description: Describes the type of property bag.
old-location: fsrm\fsrmpropertybagfield.htm
tech.root: fsrm
ms.assetid: 7a8cd6a6-7933-4190-b4fc-1b1cd653bd14
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmPropertyBagField, FsrmPropertyBagField enumeration [File Server Resource Manager], FsrmPropertyBagField_AccessVolume, FsrmPropertyBagField_VolumeGuidName, fs.fsrmpropertybagfield, fsrm.fsrmpropertybagfield, fsrmenums/FsrmPropertyBagField, fsrmenums/FsrmPropertyBagField_AccessVolume, fsrmenums/FsrmPropertyBagField_VolumeGuidName
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmPropertyBagField
product: Windows
targetos: Windows
req.typenames: FsrmPropertyBagField
req.redist: 
ms.custom: 19H1
---

# FsrmPropertyBagField enumeration


## -description


Describes the type of property bag.


## -enum-fields




### -field FsrmPropertyBagField_AccessVolume

Indicates if the property bag should include the name of the volume being accessed, which may be a 
      snapshot.


### -field FsrmPropertyBagField_VolumeGuidName

Indicates if the property bag should include the volume <b>GUID</b> name of the 
      original volume.


## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>



<a href="https://msdn.microsoft.com/ccd52bbc-998e-435f-bea5-ed456adf3ff9">IFsrmPropertyBag2::GetFieldValue</a>
 

 

