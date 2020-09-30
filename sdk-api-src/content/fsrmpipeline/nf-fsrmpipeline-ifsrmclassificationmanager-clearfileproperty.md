---
UID: NF:fsrmpipeline.IFsrmClassificationManager.ClearFileProperty
title: IFsrmClassificationManager::ClearFileProperty (fsrmpipeline.h)
description: Attempts to remove the specified property from the file or folder.
helpviewer_keywords: ["ClearFileProperty","ClearFileProperty method [File Server Resource Manager]","ClearFileProperty method [File Server Resource Manager]","FsrmClassificationManager class","ClearFileProperty method [File Server Resource Manager]","IFsrmClassificationManager interface","ClearFileProperty method [File Server Resource Manager]","IFsrmClassificationManager2 interface","FsrmClassificationManager class [File Server Resource Manager]","ClearFileProperty method","IFsrmClassificationManager interface [File Server Resource Manager]","ClearFileProperty method","IFsrmClassificationManager.ClearFileProperty","IFsrmClassificationManager2 interface [File Server Resource Manager]","ClearFileProperty method","IFsrmClassificationManager2::ClearFileProperty","IFsrmClassificationManager::ClearFileProperty","fs.ifsrmclassificationmanager_clearfileproperty","fsrm.ifsrmclassificationmanager_clearfileproperty","fsrmpipeline/IFsrmClassificationManager2::ClearFileProperty","fsrmpipeline/IFsrmClassificationManager::ClearFileProperty"]
old-location: fsrm\ifsrmclassificationmanager_clearfileproperty.htm
tech.root: fsrm
ms.assetid: bac42416-0757-462f-8869-339655f48587
ms.date: 12/05/2018
ms.keywords: ClearFileProperty, ClearFileProperty method [File Server Resource Manager], ClearFileProperty method [File Server Resource Manager],FsrmClassificationManager class, ClearFileProperty method [File Server Resource Manager],IFsrmClassificationManager interface, ClearFileProperty method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],ClearFileProperty method, IFsrmClassificationManager interface [File Server Resource Manager],ClearFileProperty method, IFsrmClassificationManager.ClearFileProperty, IFsrmClassificationManager2 interface [File Server Resource Manager],ClearFileProperty method, IFsrmClassificationManager2::ClearFileProperty, IFsrmClassificationManager::ClearFileProperty, fs.ifsrmclassificationmanager_clearfileproperty, fsrm.ifsrmclassificationmanager_clearfileproperty, fsrmpipeline/IFsrmClassificationManager2::ClearFileProperty, fsrmpipeline/IFsrmClassificationManager::ClearFileProperty
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
 - IFsrmClassificationManager::ClearFileProperty
 - fsrmpipeline/IFsrmClassificationManager::ClearFileProperty
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
 - IFsrmClassificationManager.ClearFileProperty
 - IFsrmClassificationManager2.ClearFileProperty
 - FsrmClassificationManager.ClearFileProperty
---

# IFsrmClassificationManager::ClearFileProperty


## -description

Attempts to remove the specified property from the file or folder.

<b>Windows Server 2008 R2:  </b>Only files are supported until Windows Server 2012.

## -parameters

### -param filePath [in]

The file that contains the property that you want to remove. You must specify an absolute path to the file. 
      You cannot specify a file share.

### -param property [in]

The name of the property to remove from the file.

## -returns

The method returns the following return values.

## -remarks

The property is removed from the file if the storage module is able to remove the property; otherwise, the 
     property's value is cleared using the values in the following list.

<table>
<tr>
<th>Property type</th>
<th>Cleared value</th>
</tr>
<tr>
<td>Boolean</td>
<td></td>
</tr>
<tr>
<td>Date</td>
<td></td>
</tr>
<tr>
<td>Hierarchy</td>
<td></td>
</tr>
<tr>
<td>Integer</td>
<td></td>
</tr>
<tr>
<td>Multiple choice list</td>
<td></td>
</tr>
<tr>
<td>Single choice list</td>
<td></td>
</tr>
<tr>
<td>Multi-string</td>
<td></td>
</tr>
<tr>
<td>Ordered list</td>
<td></td>
</tr>
<tr>
<td>String</td>
<td>Empty string</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getfileproperty">IFsrmClassificationManager::GetFileProperty</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-setfileproperty">IFsrmClassificationManager::SetFileProperty</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>