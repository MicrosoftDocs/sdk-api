---
UID: NF:fsrmpipeline.IFsrmClassificationManager.GetPropertyDefinition
title: IFsrmClassificationManager::GetPropertyDefinition (fsrmpipeline.h)
description: Retrieves the specified property definition.
helpviewer_keywords: ["FsrmClassificationManager class [File Server Resource Manager]","GetPropertyDefinition method","GetPropertyDefinition","GetPropertyDefinition method [File Server Resource Manager]","GetPropertyDefinition method [File Server Resource Manager]","FsrmClassificationManager class","GetPropertyDefinition method [File Server Resource Manager]","IFsrmClassificationManager interface","GetPropertyDefinition method [File Server Resource Manager]","IFsrmClassificationManager2 interface","IFsrmClassificationManager interface [File Server Resource Manager]","GetPropertyDefinition method","IFsrmClassificationManager.GetPropertyDefinition","IFsrmClassificationManager2 interface [File Server Resource Manager]","GetPropertyDefinition method","IFsrmClassificationManager2::GetPropertyDefinition","IFsrmClassificationManager::GetPropertyDefinition","fs.ifsrmclassificationmanager_getpropertydefinition","fsrm.ifsrmclassificationmanager_getpropertydefinition","fsrmpipeline/IFsrmClassificationManager2::GetPropertyDefinition","fsrmpipeline/IFsrmClassificationManager::GetPropertyDefinition"]
old-location: fsrm\ifsrmclassificationmanager_getpropertydefinition.htm
tech.root: fsrm
ms.assetid: de89524d-70b7-4f0a-add0-d34d54bd32a7
ms.date: 12/05/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],GetPropertyDefinition method, GetPropertyDefinition, GetPropertyDefinition method [File Server Resource Manager], GetPropertyDefinition method [File Server Resource Manager],FsrmClassificationManager class, GetPropertyDefinition method [File Server Resource Manager],IFsrmClassificationManager interface, GetPropertyDefinition method [File Server Resource Manager],IFsrmClassificationManager2 interface, IFsrmClassificationManager interface [File Server Resource Manager],GetPropertyDefinition method, IFsrmClassificationManager.GetPropertyDefinition, IFsrmClassificationManager2 interface [File Server Resource Manager],GetPropertyDefinition method, IFsrmClassificationManager2::GetPropertyDefinition, IFsrmClassificationManager::GetPropertyDefinition, fs.ifsrmclassificationmanager_getpropertydefinition, fsrm.ifsrmclassificationmanager_getpropertydefinition, fsrmpipeline/IFsrmClassificationManager2::GetPropertyDefinition, fsrmpipeline/IFsrmClassificationManager::GetPropertyDefinition
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
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
 - IFsrmClassificationManager::GetPropertyDefinition
 - fsrmpipeline/IFsrmClassificationManager::GetPropertyDefinition
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
 - IFsrmClassificationManager.GetPropertyDefinition
 - IFsrmClassificationManager2.GetPropertyDefinition
 - FsrmClassificationManager.GetPropertyDefinition
---

# IFsrmClassificationManager::GetPropertyDefinition


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Retrieves the specified property definition.

## -parameters

### -param propertyName [in]

The name of the property definition to retrieve.

### -param propertyDefinition [out]

An <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertydefinition">IFsrmPropertyDefinition</a> interface to the 
      retrieved property definition.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createpropertydefinition">IFsrmClassificationManager::CreatePropertyDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumpropertydefinitions">IFsrmClassificationManager::EnumPropertyDefinitions</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>