---
UID: NF:fsrmpipeline.IFsrmPropertyBag.get_RelativeNamespaceRoot
title: IFsrmPropertyBag::get_RelativeNamespaceRoot (fsrmpipeline.h)
description: The relative path of the namespace root under which the file is being evaluated.
helpviewer_keywords: ["IFsrmPropertyBag interface [File Server Resource Manager]","RelativeNamespaceRoot property","IFsrmPropertyBag.RelativeNamespaceRoot","IFsrmPropertyBag.get_RelativeNamespaceRoot","IFsrmPropertyBag::RelativeNamespaceRoot","IFsrmPropertyBag::get_RelativeNamespaceRoot","RelativeNamespaceRoot property [File Server Resource Manager]","RelativeNamespaceRoot property [File Server Resource Manager]","IFsrmPropertyBag interface","fs.ifsrmpropertybag_relativenamespaceroot","fsrm.ifsrmpropertybag_relativenamespaceroot","fsrmpipeline/IFsrmPropertyBag::RelativeNamespaceRoot","fsrmpipeline/IFsrmPropertyBag::get_RelativeNamespaceRoot","get_RelativeNamespaceRoot"]
old-location: fsrm\ifsrmpropertybag_relativenamespaceroot.htm
tech.root: fsrm
ms.assetid: 31e0baad-286a-42f3-bd30-84fc40c935f6
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyBag interface [File Server Resource Manager],RelativeNamespaceRoot property, IFsrmPropertyBag.RelativeNamespaceRoot, IFsrmPropertyBag.get_RelativeNamespaceRoot, IFsrmPropertyBag::RelativeNamespaceRoot, IFsrmPropertyBag::get_RelativeNamespaceRoot, RelativeNamespaceRoot property [File Server Resource Manager], RelativeNamespaceRoot property [File Server Resource Manager],IFsrmPropertyBag interface, fs.ifsrmpropertybag_relativenamespaceroot, fsrm.ifsrmpropertybag_relativenamespaceroot, fsrmpipeline/IFsrmPropertyBag::RelativeNamespaceRoot, fsrmpipeline/IFsrmPropertyBag::get_RelativeNamespaceRoot, get_RelativeNamespaceRoot
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
 - IFsrmPropertyBag::get_RelativeNamespaceRoot
 - fsrmpipeline/IFsrmPropertyBag::get_RelativeNamespaceRoot
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
 - IFsrmPropertyBag.RelativeNamespaceRoot
 - IFsrmPropertyBag.get_RelativeNamespaceRoot
---

# IFsrmPropertyBag::get_RelativeNamespaceRoot


## -description

The relative path of the namespace root under which the file is being evaluated.

This property is read-only.

## -parameters

## -remarks

This property is only valid under an evaluation context. Classifier modules that retrieve this property will get the namespace root of the rule under which the file is being evaluated. Because storage modules do not have evaluation contexts, they must not retrieve this property.

The relative namespace root is the path of the namespace root relative to the volume root.  For example, if the path to the file is "P:\folder1\subfolderA\test.txt", and the file is being evaluated by a rule with a namespace root of "P:\folder1", then the relative namespace root would be "\folder1\". Note that the rule's namespace root determines the relative namespace root.

The caller should not expect that the relative namespace root returned will consistently have leading or trailing backslashes.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertybag">IFsrmPropertyBag</a>