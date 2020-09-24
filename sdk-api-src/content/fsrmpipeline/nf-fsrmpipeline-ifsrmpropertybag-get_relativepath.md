---
UID: NF:fsrmpipeline.IFsrmPropertyBag.get_RelativePath
title: IFsrmPropertyBag::get_RelativePath (fsrmpipeline.h)
description: The relative path to the file.
helpviewer_keywords: ["IFsrmPropertyBag interface [File Server Resource Manager]","RelativePath property","IFsrmPropertyBag.RelativePath","IFsrmPropertyBag.get_RelativePath","IFsrmPropertyBag::RelativePath","IFsrmPropertyBag::get_RelativePath","RelativePath property [File Server Resource Manager]","RelativePath property [File Server Resource Manager]","IFsrmPropertyBag interface","fs.ifsrmpropertybag_relativepath","fsrm.ifsrmpropertybag_relativepath","fsrmpipeline/IFsrmPropertyBag::RelativePath","fsrmpipeline/IFsrmPropertyBag::get_RelativePath","get_RelativePath"]
old-location: fsrm\ifsrmpropertybag_relativepath.htm
tech.root: fsrm
ms.assetid: 4304228a-5e8e-4e2d-9fc9-48777cb23251
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyBag interface [File Server Resource Manager],RelativePath property, IFsrmPropertyBag.RelativePath, IFsrmPropertyBag.get_RelativePath, IFsrmPropertyBag::RelativePath, IFsrmPropertyBag::get_RelativePath, RelativePath property [File Server Resource Manager], RelativePath property [File Server Resource Manager],IFsrmPropertyBag interface, fs.ifsrmpropertybag_relativepath, fsrm.ifsrmpropertybag_relativepath, fsrmpipeline/IFsrmPropertyBag::RelativePath, fsrmpipeline/IFsrmPropertyBag::get_RelativePath, get_RelativePath
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
 - IFsrmPropertyBag::get_RelativePath
 - fsrmpipeline/IFsrmPropertyBag::get_RelativePath
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
 - IFsrmPropertyBag.RelativePath
 - IFsrmPropertyBag.get_RelativePath
---

# IFsrmPropertyBag::get_RelativePath


## -description

The relative path to the file.

This property is read-only.

## -parameters

## -remarks

The relative path is the path of the file relative to the volume root.  For example, if the path to the file is "P:\folder1\subfolderA\test.txt", the relative path would be "\folder1\subfolderA".

The caller should not expect that the relative path returned will consistently have leading or trailing backslashes.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertybag">IFsrmPropertyBag</a>