---
UID: NF:fsrmpipeline.IFsrmClassificationManager.CreateModuleDefinition
title: IFsrmClassificationManager::CreateModuleDefinition (fsrmpipeline.h)
description: Creates a module definition of the specified type.
helpviewer_keywords: ["CreateModuleDefinition","CreateModuleDefinition method [File Server Resource Manager]","CreateModuleDefinition method [File Server Resource Manager]","FsrmClassificationManager class","CreateModuleDefinition method [File Server Resource Manager]","IFsrmClassificationManager interface","CreateModuleDefinition method [File Server Resource Manager]","IFsrmClassificationManager2 interface","FsrmClassificationManager class [File Server Resource Manager]","CreateModuleDefinition method","IFsrmClassificationManager interface [File Server Resource Manager]","CreateModuleDefinition method","IFsrmClassificationManager.CreateModuleDefinition","IFsrmClassificationManager2 interface [File Server Resource Manager]","CreateModuleDefinition method","IFsrmClassificationManager2::CreateModuleDefinition","IFsrmClassificationManager::CreateModuleDefinition","fs.ifsrmclassificationmanager_createmoduledefinition","fsrm.ifsrmclassificationmanager_createmoduledefinition","fsrmpipeline/IFsrmClassificationManager2::CreateModuleDefinition","fsrmpipeline/IFsrmClassificationManager::CreateModuleDefinition"]
old-location: fsrm\ifsrmclassificationmanager_createmoduledefinition.htm
tech.root: fsrm
ms.assetid: 1964f4b6-b4e0-45a2-aca1-2e3dc44745a4
ms.date: 12/05/2018
ms.keywords: CreateModuleDefinition, CreateModuleDefinition method [File Server Resource Manager], CreateModuleDefinition method [File Server Resource Manager],FsrmClassificationManager class, CreateModuleDefinition method [File Server Resource Manager],IFsrmClassificationManager interface, CreateModuleDefinition method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],CreateModuleDefinition method, IFsrmClassificationManager interface [File Server Resource Manager],CreateModuleDefinition method, IFsrmClassificationManager.CreateModuleDefinition, IFsrmClassificationManager2 interface [File Server Resource Manager],CreateModuleDefinition method, IFsrmClassificationManager2::CreateModuleDefinition, IFsrmClassificationManager::CreateModuleDefinition, fs.ifsrmclassificationmanager_createmoduledefinition, fsrm.ifsrmclassificationmanager_createmoduledefinition, fsrmpipeline/IFsrmClassificationManager2::CreateModuleDefinition, fsrmpipeline/IFsrmClassificationManager::CreateModuleDefinition
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
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
 - IFsrmClassificationManager::CreateModuleDefinition
 - fsrmpipeline/IFsrmClassificationManager::CreateModuleDefinition
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
 - IFsrmClassificationManager.CreateModuleDefinition
 - IFsrmClassificationManager2.CreateModuleDefinition
 - FsrmClassificationManager.CreateModuleDefinition
---

# IFsrmClassificationManager::CreateModuleDefinition


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Creates a module definition of the specified type.

## -parameters

### -param moduleType [in]

The type of module to create (for example, a classifier or storage module). For possible types, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpipelinemoduletype">FsrmPipelineModuleType</a> enumeration.

### -param moduleDefinition [out]

An <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduledefinition">IFsrmPipelineModuleDefinition</a> 
       interface to the new module definition. Query the 
       <b>IFsrmPipelineModuleDefinition</b> interface to 
       get the interface for the specified module. For example, if <i>moduleType</i> is 
       <b>FsrmPipelineModuleType_Classifier</b>, query the 
       <b>IFsrmPipelineModuleDefinition</b> interface 
       for the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduledefinition">IFsrmClassifierModuleDefinition</a> 
       interface.

To save the module definition, call 
       <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmPipelineModuleDefinition::Commit</a> method.

## -returns

The method returns the following return values.

## -remarks

There is no limit to the number of modules that you can define.

In addition to defining the module with FSRM, you must also register the class with COM. This needs to be a 
    registration of a COM class that implements 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a> or 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>, 
    depending on the type of module.

FSRM provides the following built-in classifiers: the Folder Classifier and the Content Classifier. The Folder 
    Classifier classifies files based on the folder in which they are stored. The Content Classifier classifies by 
    searching for strings and regular expressions in the file using Windows text extraction methods.

FSRM provides the following three built-in storage modules:

<ul>
<li>System Cache Storage Module—stores properties in an NTFS Alternate Data Stream 
      cache.</li>
<li>Office 97 - 2003 In-File Storage Module—stores properties within a Microsoft Office 
      97 - 2003 file.</li>
<li>Office 2007 In-File Storage Module—stores properties within a Microsoft Office 
      2007 (or later) file.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enummoduledefinitions">IFsrmClassificationManager::EnumModuleDefinitions</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getmoduledefinition">IFsrmClassificationManager::GetModuleDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduledefinition">IFsrmClassifierModuleDefinition</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduleconnector-bind">IFsrmPipelineModuleConnector::Bind</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduledefinition">IFsrmStorageModuleDefinition</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>