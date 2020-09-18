---
UID: NF:fsrmpipeline.IFsrmClassificationManager.GetFileProperty
title: IFsrmClassificationManager::GetFileProperty (fsrmpipeline.h)
description: Retrieves the specified property from the file or folder.
helpviewer_keywords: ["FsrmClassificationManager class [File Server Resource Manager]","GetFileProperty method","GetFileProperty","GetFileProperty method [File Server Resource Manager]","GetFileProperty method [File Server Resource Manager]","FsrmClassificationManager class","GetFileProperty method [File Server Resource Manager]","IFsrmClassificationManager interface","GetFileProperty method [File Server Resource Manager]","IFsrmClassificationManager2 interface","IFsrmClassificationManager interface [File Server Resource Manager]","GetFileProperty method","IFsrmClassificationManager.GetFileProperty","IFsrmClassificationManager2 interface [File Server Resource Manager]","GetFileProperty method","IFsrmClassificationManager2::GetFileProperty","IFsrmClassificationManager::GetFileProperty","fs.ifsrmclassificationmanager_getfileproperty","fsrm.ifsrmclassificationmanager_getfileproperty","fsrmpipeline/IFsrmClassificationManager2::GetFileProperty","fsrmpipeline/IFsrmClassificationManager::GetFileProperty"]
old-location: fsrm\ifsrmclassificationmanager_getfileproperty.htm
tech.root: fsrm
ms.assetid: c8a3c4cb-4753-495b-88f4-2d6cdfef7dc7
ms.date: 12/05/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],GetFileProperty method, GetFileProperty, GetFileProperty method [File Server Resource Manager], GetFileProperty method [File Server Resource Manager],FsrmClassificationManager class, GetFileProperty method [File Server Resource Manager],IFsrmClassificationManager interface, GetFileProperty method [File Server Resource Manager],IFsrmClassificationManager2 interface, IFsrmClassificationManager interface [File Server Resource Manager],GetFileProperty method, IFsrmClassificationManager.GetFileProperty, IFsrmClassificationManager2 interface [File Server Resource Manager],GetFileProperty method, IFsrmClassificationManager2::GetFileProperty, IFsrmClassificationManager::GetFileProperty, fs.ifsrmclassificationmanager_getfileproperty, fsrm.ifsrmclassificationmanager_getfileproperty, fsrmpipeline/IFsrmClassificationManager2::GetFileProperty, fsrmpipeline/IFsrmClassificationManager::GetFileProperty
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
 - IFsrmClassificationManager::GetFileProperty
 - fsrmpipeline/IFsrmClassificationManager::GetFileProperty
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
 - IFsrmClassificationManager.GetFileProperty
 - IFsrmClassificationManager2.GetFileProperty
 - FsrmClassificationManager.GetFileProperty
---

# IFsrmClassificationManager::GetFileProperty


## -description

Retrieves the specified property from the file or folder.

<b>Windows Server 2008 R2:  </b>Only files are supported until Windows Server 2012.

## -parameters

### -param filePath [in]

The file that contains the property that you want to retrieve. You must specify an absolute path to the 
      file. You cannot specify a file share.

### -param propertyName [in]

The name of the property to retrieve. Must not exceed 100 characters in length.

### -param options [in]

The option to use for retrieving the file's property. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmgetfilepropertyoptions">FsrmGetFilePropertyOptions</a> enumeration.

### -param property [out]

An <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmproperty">IFsrmProperty</a> interface to  the retrieved 
      property.

## -returns

The method returns the following return values.

## -remarks

FSRM asks the specified storage modules (see the <i>options</i> parameter) to retrieve the 
    property from the file. If the <i>options</i> parameter is set to 
    <b>FsrmGetFilePropertyOptions_None</b>, FSRM reruns classification on the file to ensure the 
    correct value is returned.


#### Examples

For examples in C# and PowerShell see 
     <a href="/previous-versions/windows/desktop/fsrm/accessing-classification-properties">Accessing Classification Properties</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-clearfileproperty">IFsrmClassificationManager::ClearFileProperty</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumfileproperties">IFsrmClassificationManager::EnumFileProperties</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-setfileproperty">IFsrmClassificationManager::SetFileProperty</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>