---
UID: NF:fsrmpipeline.IFsrmClassificationManager.EnumFileProperties
title: IFsrmClassificationManager::EnumFileProperties (fsrmpipeline.h)
description: Enumerates the properties of the specified file.
helpviewer_keywords: ["EnumFileProperties","EnumFileProperties method [File Server Resource Manager]","EnumFileProperties method [File Server Resource Manager]","FsrmClassificationManager class","EnumFileProperties method [File Server Resource Manager]","IFsrmClassificationManager interface","EnumFileProperties method [File Server Resource Manager]","IFsrmClassificationManager2 interface","FsrmClassificationManager class [File Server Resource Manager]","EnumFileProperties method","IFsrmClassificationManager interface [File Server Resource Manager]","EnumFileProperties method","IFsrmClassificationManager.EnumFileProperties","IFsrmClassificationManager2 interface [File Server Resource Manager]","EnumFileProperties method","IFsrmClassificationManager2::EnumFileProperties","IFsrmClassificationManager::EnumFileProperties","fs.ifsrmclassificationmanager_enumfileproperties","fsrm.ifsrmclassificationmanager_enumfileproperties","fsrmpipeline/IFsrmClassificationManager2::EnumFileProperties","fsrmpipeline/IFsrmClassificationManager::EnumFileProperties"]
old-location: fsrm\ifsrmclassificationmanager_enumfileproperties.htm
tech.root: fsrm
ms.assetid: 9a833e94-d26b-4c94-bf2f-76ac6db3f8e9
ms.date: 12/05/2018
ms.keywords: EnumFileProperties, EnumFileProperties method [File Server Resource Manager], EnumFileProperties method [File Server Resource Manager],FsrmClassificationManager class, EnumFileProperties method [File Server Resource Manager],IFsrmClassificationManager interface, EnumFileProperties method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],EnumFileProperties method, IFsrmClassificationManager interface [File Server Resource Manager],EnumFileProperties method, IFsrmClassificationManager.EnumFileProperties, IFsrmClassificationManager2 interface [File Server Resource Manager],EnumFileProperties method, IFsrmClassificationManager2::EnumFileProperties, IFsrmClassificationManager::EnumFileProperties, fs.ifsrmclassificationmanager_enumfileproperties, fsrm.ifsrmclassificationmanager_enumfileproperties, fsrmpipeline/IFsrmClassificationManager2::EnumFileProperties, fsrmpipeline/IFsrmClassificationManager::EnumFileProperties
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
 - IFsrmClassificationManager::EnumFileProperties
 - fsrmpipeline/IFsrmClassificationManager::EnumFileProperties
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
 - IFsrmClassificationManager.EnumFileProperties
 - IFsrmClassificationManager2.EnumFileProperties
 - FsrmClassificationManager.EnumFileProperties
---

# IFsrmClassificationManager::EnumFileProperties


## -description

Enumerates the properties of the specified file.

## -parameters

### -param filePath [in]

The file that contains the properties that you want to enumerate. You must specify an absolute path to the 
      file. You cannot specify a file share.

### -param options [in]

The option to use for enumerating the file's properties. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmgetfilepropertyoptions">FsrmGetFilePropertyOptions</a> enumeration.

### -param fileProperties [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> interface that contains a 
      collection of file properties. Each item in the collection is a <b>VARIANT</b> of type 
      <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
      the <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmproperty">IFsrmProperty</a> interface.

## -returns

The method returns the following return values.

## -remarks

FSRM asks the specified storage modules (see the <i>options</i> parameter) to return all 
    the properties for the file for which they are responsible. For storage modules that embed the properties in the 
    file, the list will include all properties embedded in the file (not just those defined by FSRM).

If the <i>options</i> parameter is set to 
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



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getfileproperty">IFsrmClassificationManager::GetFileProperty</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-setfileproperty">IFsrmClassificationManager::SetFileProperty</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>