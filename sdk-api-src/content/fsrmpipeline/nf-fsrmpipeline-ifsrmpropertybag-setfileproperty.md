---
UID: NF:fsrmpipeline.IFsrmPropertyBag.SetFileProperty
title: IFsrmPropertyBag::SetFileProperty (fsrmpipeline.h)
description: Sets the specified property in the property bag.
helpviewer_keywords: ["IFsrmPropertyBag interface [File Server Resource Manager]","SetFileProperty method","IFsrmPropertyBag.SetFileProperty","IFsrmPropertyBag::SetFileProperty","SetFileProperty","SetFileProperty method [File Server Resource Manager]","SetFileProperty method [File Server Resource Manager]","IFsrmPropertyBag interface","fs.ifsrmpropertybag_setfileproperty","fsrm.ifsrmpropertybag_setfileproperty","fsrmpipeline/IFsrmPropertyBag::SetFileProperty"]
old-location: fsrm\ifsrmpropertybag_setfileproperty.htm
tech.root: fsrm
ms.assetid: d3322907-c832-49ef-bf21-2e4581251a88
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyBag interface [File Server Resource Manager],SetFileProperty method, IFsrmPropertyBag.SetFileProperty, IFsrmPropertyBag::SetFileProperty, SetFileProperty, SetFileProperty method [File Server Resource Manager], SetFileProperty method [File Server Resource Manager],IFsrmPropertyBag interface, fs.ifsrmpropertybag_setfileproperty, fsrm.ifsrmpropertybag_setfileproperty, fsrmpipeline/IFsrmPropertyBag::SetFileProperty
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
 - IFsrmPropertyBag::SetFileProperty
 - fsrmpipeline/IFsrmPropertyBag::SetFileProperty
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
 - IFsrmPropertyBag.SetFileProperty
---

# IFsrmPropertyBag::SetFileProperty


## -description

Sets the specified property in the property bag.

## -parameters

### -param name [in]

The name of the property to set.

### -param value [in]

The value to set the property to.

## -returns

The method returns the following return values.

## -remarks

The caller must be a storage module to obtain access to this property.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertybag">IFsrmPropertyBag</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-getfileproperty">IFsrmPropertyBag::GetFileProperty</a>