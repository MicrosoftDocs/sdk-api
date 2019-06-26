---
UID: NF:fsrmpipeline.IFsrmClassificationRule.put_PropertyAffected
title: IFsrmClassificationRule::put_PropertyAffected (fsrmpipeline.h)
author: windows-sdk-content
description: The name of the property that this rule affects.
old-location: fsrm\ifsrmclassificationrule_propertyaffected.htm
tech.root: fsrm
ms.assetid: 0e41ac2b-c48a-4bb8-a363-8a64c856b8f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmClassificationRule interface [File Server Resource Manager],PropertyAffected property, IFsrmClassificationRule.PropertyAffected, IFsrmClassificationRule.put_PropertyAffected, IFsrmClassificationRule::PropertyAffected, IFsrmClassificationRule::get_PropertyAffected, IFsrmClassificationRule::put_PropertyAffected, PropertyAffected property [File Server Resource Manager], PropertyAffected property [File Server Resource Manager],IFsrmClassificationRule interface, fs.ifsrmclassificationrule_propertyaffected, fsrm.ifsrmclassificationrule_propertyaffected, fsrmpipeline/IFsrmClassificationRule::PropertyAffected, fsrmpipeline/IFsrmClassificationRule::get_PropertyAffected, fsrmpipeline/IFsrmClassificationRule::put_PropertyAffected, put_PropertyAffected
ms.topic: method
f1_keywords: 
 - "fsrmpipeline/IFsrmClassificationRule.PropertyAffected"
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
 - IFsrmClassificationRule.PropertyAffected
 - IFsrmClassificationRule.get_PropertyAffected
 - IFsrmClassificationRule.put_PropertyAffected
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmClassificationRule::put_PropertyAffected


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmclassificationrule">MSFT_FSRMClassificationRule</a> class.]

The name of the property that this rule affects.

This property is read/write.


## -parameters


## -remarks



If the classifier specifies a list of properties that it affects (see 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduledefinition-get_propertiesaffected">IFsrmClassifierModuleDefinition::PropertiesAffected</a>), the property that you specify must exist in the list of affected properties.

To enumerate the properties that have been defined, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumpropertydefinitions">IFsrmClassificationManager::EnumPropertyDefinitions</a> method. To access the name of the property, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertydefinition-get_name">IFsrmPropertyDefinition.Name</a> 
    property.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationrule">IFsrmClassificationRule</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmclassificationrule">MSFT_FSRMClassificationRule</a>
 

 

