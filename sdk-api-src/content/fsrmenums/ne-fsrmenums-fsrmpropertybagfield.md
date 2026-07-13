---
UID: NE:fsrmenums._FsrmPropertyBagField
title: FsrmPropertyBagField (fsrmenums.h)
description: Describes the type of property bag.
helpviewer_keywords: ["FsrmPropertyBagField","FsrmPropertyBagField enumeration [File Server Resource Manager]","FsrmPropertyBagField_AccessVolume","FsrmPropertyBagField_VolumeGuidName","fs.fsrmpropertybagfield","fsrm.fsrmpropertybagfield","fsrmenums/FsrmPropertyBagField","fsrmenums/FsrmPropertyBagField_AccessVolume","fsrmenums/FsrmPropertyBagField_VolumeGuidName"]
old-location: fsrm\fsrmpropertybagfield.htm
tech.root: fsrm
ms.assetid: 7a8cd6a6-7933-4190-b4fc-1b1cd653bd14
ms.date: 12/05/2018
ms.keywords: FsrmPropertyBagField, FsrmPropertyBagField enumeration [File Server Resource Manager], FsrmPropertyBagField_AccessVolume, FsrmPropertyBagField_VolumeGuidName, fs.fsrmpropertybagfield, fsrm.fsrmpropertybagfield, fsrmenums/FsrmPropertyBagField, fsrmenums/FsrmPropertyBagField_AccessVolume, fsrmenums/FsrmPropertyBagField_VolumeGuidName
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
targetos: Windows
req.typenames: FsrmPropertyBagField
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmPropertyBagField
 - fsrmenums/_FsrmPropertyBagField
 - FsrmPropertyBagField
 - fsrmenums/FsrmPropertyBagField
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
 - FsrmPropertyBagField
---

# FsrmPropertyBagField enumeration


## -description

Describes the type of property bag.

## -enum-fields

### -field FsrmPropertyBagField_AccessVolume:0

Indicates if the property bag should include the name of the volume being accessed, which may be a 
      snapshot.

### -field FsrmPropertyBagField_VolumeGuidName:1

Indicates if the property bag should include the volume <b>GUID</b> name of the 
      original volume.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag2-getfieldvalue">IFsrmPropertyBag2::GetFieldValue</a>
