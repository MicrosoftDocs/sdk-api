---
UID: NF:fsrmpipeline.IFsrmClassificationRule.get_Value
title: IFsrmClassificationRule::get_Value
author: windows-sdk-content
description: The value that this rule will set the property to.
old-location: fsrm\ifsrmclassificationrule_value.htm
tech.root: fsrm
ms.assetid: c243cf7a-23f5-4d81-acea-9bf6ed66967d
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: IFsrmClassificationRule interface [File Server Resource Manager],Value property, IFsrmClassificationRule.Value, IFsrmClassificationRule.get_Value, IFsrmClassificationRule::Value, IFsrmClassificationRule::get_Value, IFsrmClassificationRule::put_Value, Value property [File Server Resource Manager], Value property [File Server Resource Manager],IFsrmClassificationRule interface, fs.ifsrmclassificationrule_value, fsrm.ifsrmclassificationrule_value, fsrmpipeline/IFsrmClassificationRule::Value, fsrmpipeline/IFsrmClassificationRule::get_Value, fsrmpipeline/IFsrmClassificationRule::put_Value, get_Value
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmClassificationRule::get_Value


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/845fc1e8-d06a-4bc4-9529-0748cb488727">MSFT_FSRMClassificationRule</a> class.]

The value that this rule will set the property to.

This property is read/write.


## -parameters


## -remarks



The classifier determines whether you must specify a value. If the classifier sets the 
    <a href="https://msdn.microsoft.com/580542ef-c766-4a39-9dbd-aed2f4a11780">IFsrmClassifierModuleDefinition.NeedsExplicitValue</a> 
    property to <b>VARIANT_TRUE</b>, then you must provide a value; otherwise, the classifier 
    determines the value to set the property's value to (do not set this property).




## -see-also




<a href="https://msdn.microsoft.com/d76e4b07-66d6-426f-853d-f52ea08d9b81">IFsrmClassificationRule</a>



<a href="https://msdn.microsoft.com/845fc1e8-d06a-4bc4-9529-0748cb488727">MSFT_FSRMClassificationRule</a>
 

 

