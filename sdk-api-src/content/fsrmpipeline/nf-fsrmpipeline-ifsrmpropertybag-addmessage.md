---
UID: NF:fsrmpipeline.IFsrmPropertyBag.AddMessage
title: IFsrmPropertyBag::AddMessage (fsrmpipeline.h)
description: Adds an error message to the bag.
helpviewer_keywords: ["AddMessage","AddMessage method [File Server Resource Manager]","AddMessage method [File Server Resource Manager]","IFsrmPropertyBag interface","IFsrmPropertyBag interface [File Server Resource Manager]","AddMessage method","IFsrmPropertyBag.AddMessage","IFsrmPropertyBag::AddMessage","fs.ifsrmpropertybag_addmessage","fsrm.ifsrmpropertybag_addmessage","fsrmpipeline/IFsrmPropertyBag::AddMessage"]
old-location: fsrm\ifsrmpropertybag_addmessage.htm
tech.root: fsrm
ms.assetid: 2d9166fd-5211-4114-843f-2c6563941715
ms.date: 12/05/2018
ms.keywords: AddMessage, AddMessage method [File Server Resource Manager], AddMessage method [File Server Resource Manager],IFsrmPropertyBag interface, IFsrmPropertyBag interface [File Server Resource Manager],AddMessage method, IFsrmPropertyBag.AddMessage, IFsrmPropertyBag::AddMessage, fs.ifsrmpropertybag_addmessage, fsrm.ifsrmpropertybag_addmessage, fsrmpipeline/IFsrmPropertyBag::AddMessage
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
 - IFsrmPropertyBag::AddMessage
 - fsrmpipeline/IFsrmPropertyBag::AddMessage
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
 - IFsrmPropertyBag.AddMessage
---

# IFsrmPropertyBag::AddMessage


## -description

Adds an error message to the bag.

## -parameters

### -param message [in]

The error message to add to the bag. The message is limited to 4096 characters (the message is truncated if longer than 4096 characters).

## -returns

The method returns the following return values.

## -remarks

You can add only one message to the bag. The message is written to the error log, if enabled.

If any of the following implementations returns an error code, FSRM automatically adds a message (which does not count against the one-message limit) that includes the error code and associated message string:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-doespropertyvalueapply">IFsrmClassifierModuleImplementation::DoesPropertyValueApply</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-getpropertyvaluetoapply">IFsrmClassifierModuleImplementation::GetPropertyValueToApply</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduleimplementation-loadproperties">IFsrmStorageModuleImplementation::LoadProperties</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduleimplementation-saveproperties">IFsrmStorageModuleImplementation::SaveProperties</a>
</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertybag">IFsrmPropertyBag</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_messages">IFsrmPropertyBag::Messages</a>