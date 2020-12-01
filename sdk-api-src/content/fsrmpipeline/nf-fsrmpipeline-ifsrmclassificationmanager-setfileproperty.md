---
UID: NF:fsrmpipeline.IFsrmClassificationManager.SetFileProperty
title: IFsrmClassificationManager::SetFileProperty (fsrmpipeline.h)
description: Sets the value of the specified property in the file or folder.
helpviewer_keywords: ["FsrmClassificationManager class [File Server Resource Manager]","SetFileProperty method","IFsrmClassificationManager interface [File Server Resource Manager]","SetFileProperty method","IFsrmClassificationManager.SetFileProperty","IFsrmClassificationManager2 interface [File Server Resource Manager]","SetFileProperty method","IFsrmClassificationManager2::SetFileProperty","IFsrmClassificationManager::SetFileProperty","SetFileProperty","SetFileProperty method [File Server Resource Manager]","SetFileProperty method [File Server Resource Manager]","FsrmClassificationManager class","SetFileProperty method [File Server Resource Manager]","IFsrmClassificationManager interface","SetFileProperty method [File Server Resource Manager]","IFsrmClassificationManager2 interface","fs.ifsrmclassificationmanager_setfileproperty","fsrm.ifsrmclassificationmanager_setfileproperty","fsrmpipeline/IFsrmClassificationManager2::SetFileProperty","fsrmpipeline/IFsrmClassificationManager::SetFileProperty"]
old-location: fsrm\ifsrmclassificationmanager_setfileproperty.htm
tech.root: fsrm
ms.assetid: 0f13f00e-6ca2-4436-822e-01eff638c446
ms.date: 12/05/2018
ms.keywords: FsrmClassificationManager class [File Server Resource Manager],SetFileProperty method, IFsrmClassificationManager interface [File Server Resource Manager],SetFileProperty method, IFsrmClassificationManager.SetFileProperty, IFsrmClassificationManager2 interface [File Server Resource Manager],SetFileProperty method, IFsrmClassificationManager2::SetFileProperty, IFsrmClassificationManager::SetFileProperty, SetFileProperty, SetFileProperty method [File Server Resource Manager], SetFileProperty method [File Server Resource Manager],FsrmClassificationManager class, SetFileProperty method [File Server Resource Manager],IFsrmClassificationManager interface, SetFileProperty method [File Server Resource Manager],IFsrmClassificationManager2 interface, fs.ifsrmclassificationmanager_setfileproperty, fsrm.ifsrmclassificationmanager_setfileproperty, fsrmpipeline/IFsrmClassificationManager2::SetFileProperty, fsrmpipeline/IFsrmClassificationManager::SetFileProperty
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
 - IFsrmClassificationManager::SetFileProperty
 - fsrmpipeline/IFsrmClassificationManager::SetFileProperty
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
 - IFsrmClassificationManager.SetFileProperty
 - IFsrmClassificationManager2.SetFileProperty
 - FsrmClassificationManager.SetFileProperty
---

# IFsrmClassificationManager::SetFileProperty


## -description

Sets the value of the specified property in the file or folder.

<b>Windows Server 2008 R2:  </b>Only files are supported until Windows Server 2012.

## -parameters

### -param filePath [in]

The file that contains the property that you want to set. You must specify an absolute path to the file. You 
      cannot specify a file share.

### -param propertyName [in]

The name of the property whose value you want to set.

### -param propertyValue [in]

The value to set the specified property to.

## -returns

The method returns the following return values.

## -remarks

The method verifies that the property value is valid for the property's type. For example, for an ordered or 
    multiple choice list, that the value is a member of the list; for a Boolean property, that the value is the string 
    "0" or "1"; and for a date, that the value is a 64-bit decimal value expressed 
    as a string.

<b>SetFileProperty</b> only 
    supports property definitions that are available on the server whose 
    <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertydefinition2-get_appliesto">AppliesTo</a> property has the 
    <b>FsrmPropertyDefinitionAppliesTo_Files</b> (1) bit set.


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



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getfileproperty">IFsrmClassificationManager::GetFileProperty</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>