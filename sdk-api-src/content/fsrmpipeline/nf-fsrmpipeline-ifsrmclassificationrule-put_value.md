---
UID: NF:fsrmpipeline.IFsrmClassificationRule.put_Value
title: IFsrmClassificationRule::put_Value (fsrmpipeline.h)
description: The value that this rule will set the property to. (Put)
helpviewer_keywords: ["IFsrmClassificationRule interface [File Server Resource Manager]","Value property","IFsrmClassificationRule.Value","IFsrmClassificationRule.put_Value","IFsrmClassificationRule::Value","IFsrmClassificationRule::get_Value","IFsrmClassificationRule::put_Value","Value property [File Server Resource Manager]","Value property [File Server Resource Manager]","IFsrmClassificationRule interface","fs.ifsrmclassificationrule_value","fsrm.ifsrmclassificationrule_value","fsrmpipeline/IFsrmClassificationRule::Value","fsrmpipeline/IFsrmClassificationRule::get_Value","fsrmpipeline/IFsrmClassificationRule::put_Value","put_Value"]
old-location: fsrm\ifsrmclassificationrule_value.htm
tech.root: fsrm
ms.assetid: c243cf7a-23f5-4d81-acea-9bf6ed66967d
ms.date: 12/05/2018
ms.keywords: IFsrmClassificationRule interface [File Server Resource Manager],Value property, IFsrmClassificationRule.Value, IFsrmClassificationRule.put_Value, IFsrmClassificationRule::Value, IFsrmClassificationRule::get_Value, IFsrmClassificationRule::put_Value, Value property [File Server Resource Manager], Value property [File Server Resource Manager],IFsrmClassificationRule interface, fs.ifsrmclassificationrule_value, fsrm.ifsrmclassificationrule_value, fsrmpipeline/IFsrmClassificationRule::Value, fsrmpipeline/IFsrmClassificationRule::get_Value, fsrmpipeline/IFsrmClassificationRule::put_Value, put_Value
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
 - IFsrmClassificationRule::put_Value
 - fsrmpipeline/IFsrmClassificationRule::put_Value
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
 - IFsrmClassificationRule.Value
 - IFsrmClassificationRule.get_Value
 - IFsrmClassificationRule.put_Value
---

# IFsrmClassificationRule::put_Value


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassificationrule">MSFT_FSRMClassificationRule</a> class.]

The value that this rule will set the property to.

This property is read/write.

## -parameters

## -remarks

The classifier determines whether you must specify a value. If the classifier sets the 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduledefinition-get_needsexplicitvalue">IFsrmClassifierModuleDefinition.NeedsExplicitValue</a> 
    property to <b>VARIANT_TRUE</b>, then you must provide a value; otherwise, the classifier 
    determines the value to set the property's value to (do not set this property).

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationrule">IFsrmClassificationRule</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassificationrule">MSFT_FSRMClassificationRule</a>
