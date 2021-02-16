---
UID: NF:fsrmpipeline.IFsrmClassificationManager.EnumPropertyDefinitions
title: IFsrmClassificationManager::EnumPropertyDefinitions (fsrmpipeline.h)
description: Enumerates the property definitions.
helpviewer_keywords: ["EnumPropertyDefinitions","EnumPropertyDefinitions method [File Server Resource Manager]","EnumPropertyDefinitions method [File Server Resource Manager]","FsrmClassificationManager class","EnumPropertyDefinitions method [File Server Resource Manager]","IFsrmClassificationManager interface","EnumPropertyDefinitions method [File Server Resource Manager]","IFsrmClassificationManager2 interface","FsrmClassificationManager class [File Server Resource Manager]","EnumPropertyDefinitions method","IFsrmClassificationManager interface [File Server Resource Manager]","EnumPropertyDefinitions method","IFsrmClassificationManager.EnumPropertyDefinitions","IFsrmClassificationManager2 interface [File Server Resource Manager]","EnumPropertyDefinitions method","IFsrmClassificationManager2::EnumPropertyDefinitions","IFsrmClassificationManager::EnumPropertyDefinitions","fs.ifsrmclassificationmanager_enumpropertydefinitions","fsrm.ifsrmclassificationmanager_enumpropertydefinitions","fsrmpipeline/IFsrmClassificationManager2::EnumPropertyDefinitions","fsrmpipeline/IFsrmClassificationManager::EnumPropertyDefinitions"]
old-location: fsrm\ifsrmclassificationmanager_enumpropertydefinitions.htm
tech.root: fsrm
ms.assetid: c97cb2f1-6e03-444e-a15e-faa85f7a7915
ms.date: 12/05/2018
ms.keywords: EnumPropertyDefinitions, EnumPropertyDefinitions method [File Server Resource Manager], EnumPropertyDefinitions method [File Server Resource Manager],FsrmClassificationManager class, EnumPropertyDefinitions method [File Server Resource Manager],IFsrmClassificationManager interface, EnumPropertyDefinitions method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],EnumPropertyDefinitions method, IFsrmClassificationManager interface [File Server Resource Manager],EnumPropertyDefinitions method, IFsrmClassificationManager.EnumPropertyDefinitions, IFsrmClassificationManager2 interface [File Server Resource Manager],EnumPropertyDefinitions method, IFsrmClassificationManager2::EnumPropertyDefinitions, IFsrmClassificationManager::EnumPropertyDefinitions, fs.ifsrmclassificationmanager_enumpropertydefinitions, fsrm.ifsrmclassificationmanager_enumpropertydefinitions, fsrmpipeline/IFsrmClassificationManager2::EnumPropertyDefinitions, fsrmpipeline/IFsrmClassificationManager::EnumPropertyDefinitions
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
 - IFsrmClassificationManager::EnumPropertyDefinitions
 - fsrmpipeline/IFsrmClassificationManager::EnumPropertyDefinitions
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
 - IFsrmClassificationManager.EnumPropertyDefinitions
 - IFsrmClassificationManager2.EnumPropertyDefinitions
 - FsrmClassificationManager.EnumPropertyDefinitions
---

# IFsrmClassificationManager::EnumPropertyDefinitions


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Enumerates the property definitions.

## -parameters

### -param options [in]

One or more options for enumerating the property definitions. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

### -param propertyDefinitions [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> interface that contains a 
       collection of property definitions. Each item in the collection is a <b>VARIANT</b> of 
       type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the 
       variant for the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpropertydefinition">IFsrmPropertyDefinition</a> 
       interface.

The collection contains only committed property definitions; the collection will not contain newly created 
       property definitions that have not been committed.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-createpropertydefinition">IFsrmClassificationManager::CreatePropertyDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getpropertydefinition">IFsrmClassificationManager::GetPropertyDefinition</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>