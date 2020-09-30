---
UID: NF:fsrmpipeline.IFsrmPropertyBag.get_Messages
title: IFsrmPropertyBag::get_Messages (fsrmpipeline.h)
description: A list of the error messages that have been added to the bag.
helpviewer_keywords: ["IFsrmPropertyBag interface [File Server Resource Manager]","Messages property","IFsrmPropertyBag.Messages","IFsrmPropertyBag.get_Messages","IFsrmPropertyBag::Messages","IFsrmPropertyBag::get_Messages","Messages property [File Server Resource Manager]","Messages property [File Server Resource Manager]","IFsrmPropertyBag interface","fs.ifsrmpropertybag_messages","fsrm.ifsrmpropertybag_messages","fsrmpipeline/IFsrmPropertyBag::Messages","fsrmpipeline/IFsrmPropertyBag::get_Messages","get_Messages"]
old-location: fsrm\ifsrmpropertybag_messages.htm
tech.root: fsrm
ms.assetid: 3aa6bc28-03bb-40ea-8c56-94133c8eeb54
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyBag interface [File Server Resource Manager],Messages property, IFsrmPropertyBag.Messages, IFsrmPropertyBag.get_Messages, IFsrmPropertyBag::Messages, IFsrmPropertyBag::get_Messages, Messages property [File Server Resource Manager], Messages property [File Server Resource Manager],IFsrmPropertyBag interface, fs.ifsrmpropertybag_messages, fsrm.ifsrmpropertybag_messages, fsrmpipeline/IFsrmPropertyBag::Messages, fsrmpipeline/IFsrmPropertyBag::get_Messages, get_Messages
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
 - IFsrmPropertyBag::get_Messages
 - fsrmpipeline/IFsrmPropertyBag::get_Messages
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
 - IFsrmPropertyBag.Messages
 - IFsrmPropertyBag.get_Messages
---

# IFsrmPropertyBag::get_Messages


## -description

A list of the error messages that have been added to the bag.

This property is read-only.

## -parameters

## -remarks

The format of the message is 
    <i>module_name</i>,<i>rule_name</i>|<i>message</i> 
    (FSRM adds the <i>module_name</i>,<i>rule_name</i>| components to the 
    message that you specified when calling the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-addmessage">IFsrmPropertyBag::AddMessage</a> method).

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertybag">IFsrmPropertyBag</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-addmessage">IFsrmPropertyBag::AddMessage</a>