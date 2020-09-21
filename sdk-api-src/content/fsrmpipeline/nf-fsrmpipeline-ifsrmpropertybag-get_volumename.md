---
UID: NF:fsrmpipeline.IFsrmPropertyBag.get_VolumeName
title: IFsrmPropertyBag::get_VolumeName (fsrmpipeline.h)
description: The name of the volume on which the file exists.
helpviewer_keywords: ["IFsrmPropertyBag interface [File Server Resource Manager]","VolumeName property","IFsrmPropertyBag.VolumeName","IFsrmPropertyBag.get_VolumeName","IFsrmPropertyBag::VolumeName","IFsrmPropertyBag::get_VolumeName","VolumeName property [File Server Resource Manager]","VolumeName property [File Server Resource Manager]","IFsrmPropertyBag interface","fs.ifsrmpropertybag_volumename","fsrm.ifsrmpropertybag_volumename","fsrmpipeline/IFsrmPropertyBag::VolumeName","fsrmpipeline/IFsrmPropertyBag::get_VolumeName","get_VolumeName"]
old-location: fsrm\ifsrmpropertybag_volumename.htm
tech.root: fsrm
ms.assetid: 65b47ad3-eb81-468e-a4fb-8a52d6b99998
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyBag interface [File Server Resource Manager],VolumeName property, IFsrmPropertyBag.VolumeName, IFsrmPropertyBag.get_VolumeName, IFsrmPropertyBag::VolumeName, IFsrmPropertyBag::get_VolumeName, VolumeName property [File Server Resource Manager], VolumeName property [File Server Resource Manager],IFsrmPropertyBag interface, fs.ifsrmpropertybag_volumename, fsrm.ifsrmpropertybag_volumename, fsrmpipeline/IFsrmPropertyBag::VolumeName, fsrmpipeline/IFsrmPropertyBag::get_VolumeName, get_VolumeName
req.header: fsrmpipeline.h
req.include-header: 
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmPropertyBag::get_VolumeName
 - fsrmpipeline/IFsrmPropertyBag::get_VolumeName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmPropertyBag.VolumeName
 - IFsrmPropertyBag.get_VolumeName
---

# IFsrmPropertyBag::get_VolumeName


## -description

The name of the volume on which the file exists.

This property is read-only.

## -parameters

## -remarks

This property contains the volume name of the location of the file being scanned. For example, if the path to a file is "P:\folder1\subfolderA\test.txt", the volume name is "P:\".

The caller should not expect that the volume name returned will consistently have a trailing backslash.

The volume name that is returned will always be the name of a live volume. In the case where the file being classified is on a snapshot, the name of the live volume that the snapshot corresponds to will be returned.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertybag">IFsrmPropertyBag</a>