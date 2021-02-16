---
UID: NF:fsrmpipeline.IFsrmPropertyBag.GetFileProperty
title: IFsrmPropertyBag::GetFileProperty (fsrmpipeline.h)
description: Retrieves the specified property from the property bag.
helpviewer_keywords: ["GetFileProperty","GetFileProperty method [File Server Resource Manager]","GetFileProperty method [File Server Resource Manager]","IFsrmPropertyBag interface","IFsrmPropertyBag interface [File Server Resource Manager]","GetFileProperty method","IFsrmPropertyBag.GetFileProperty","IFsrmPropertyBag::GetFileProperty","fs.ifsrmpropertybag_getfileproperty","fsrm.ifsrmpropertybag_getfileproperty","fsrmpipeline/IFsrmPropertyBag::GetFileProperty"]
old-location: fsrm\ifsrmpropertybag_getfileproperty.htm
tech.root: fsrm
ms.assetid: 09fc3287-f2a2-4ba7-9626-65c6634b7f2d
ms.date: 12/05/2018
ms.keywords: GetFileProperty, GetFileProperty method [File Server Resource Manager], GetFileProperty method [File Server Resource Manager],IFsrmPropertyBag interface, IFsrmPropertyBag interface [File Server Resource Manager],GetFileProperty method, IFsrmPropertyBag.GetFileProperty, IFsrmPropertyBag::GetFileProperty, fs.ifsrmpropertybag_getfileproperty, fsrm.ifsrmpropertybag_getfileproperty, fsrmpipeline/IFsrmPropertyBag::GetFileProperty
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
 - IFsrmPropertyBag::GetFileProperty
 - fsrmpipeline/IFsrmPropertyBag::GetFileProperty
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
 - IFsrmPropertyBag.GetFileProperty
---

# IFsrmPropertyBag::GetFileProperty


## -description

Retrieves the specified property from the property bag.

## -parameters

### -param name [in]

The name of the property to retrieve.

### -param fileProperty [out]

An <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmproperty">IFsrmProperty</a> interface to the retrieved property.

## -returns

The method returns the following return values.

## -remarks

Use the property name specified in the rule's <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationrule-get_propertyaffected">PropertyAffected</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertybag">IFsrmPropertyBag</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-setfileproperty">IFsrmPropertyBag::SetFileProperty</a>