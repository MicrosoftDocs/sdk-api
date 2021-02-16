---
UID: NF:fsrmpipeline.IFsrmClassificationManager2.ClassifyFiles
title: IFsrmClassificationManager2::ClassifyFiles (fsrmpipeline.h)
description: This method is used to perform bulk enumeration, setting, and clearing of file properties.
helpviewer_keywords: ["ClassifyFiles","ClassifyFiles method [File Server Resource Manager]","ClassifyFiles method [File Server Resource Manager]","FsrmClassificationManager class","ClassifyFiles method [File Server Resource Manager]","IFsrmClassificationManager2 interface","FsrmClassificationManager class [File Server Resource Manager]","ClassifyFiles method","IFsrmClassificationManager2 interface [File Server Resource Manager]","ClassifyFiles method","IFsrmClassificationManager2.ClassifyFiles","IFsrmClassificationManager2::ClassifyFiles","fs.ifsrmclassificationmanager2_classifyfiles","fsrm.ifsrmclassificationmanager2_classifyfiles","fsrmpipeline/IFsrmClassificationManager2::ClassifyFiles"]
old-location: fsrm\ifsrmclassificationmanager2_classifyfiles.htm
tech.root: fsrm
ms.assetid: 1dee9185-f83c-4e49-bf29-143271445046
ms.date: 12/05/2018
ms.keywords: ClassifyFiles, ClassifyFiles method [File Server Resource Manager], ClassifyFiles method [File Server Resource Manager],FsrmClassificationManager class, ClassifyFiles method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],ClassifyFiles method, IFsrmClassificationManager2 interface [File Server Resource Manager],ClassifyFiles method, IFsrmClassificationManager2.ClassifyFiles, IFsrmClassificationManager2::ClassifyFiles, fs.ifsrmclassificationmanager2_classifyfiles, fsrm.ifsrmclassificationmanager2_classifyfiles, fsrmpipeline/IFsrmClassificationManager2::ClassifyFiles
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmPipeline.idl
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
 - IFsrmClassificationManager2::ClassifyFiles
 - fsrmpipeline/IFsrmClassificationManager2::ClassifyFiles
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
 - IFsrmClassificationManager2.ClassifyFiles
 - FsrmClassificationManager.ClassifyFiles
---

# IFsrmClassificationManager2::ClassifyFiles


## -description

This method is used to perform bulk enumeration, setting, and clearing of file 
    properties.

## -parameters

### -param filePaths [in]

A list of the file paths.  The <b>SAFEARRAY</b> contains variants of type 
      <b>VT_BSTR</b>. For each item in the array, use the <b>bstrVal</b> member 
      to access the property name.

### -param propertyNames [in]

A list of the property names.  The <b>SAFEARRAY</b> contains variants of type 
      <b>VT_BSTR</b>. For each item in the array, use the <b>bstrVal</b> member 
      to access the property name.

### -param propertyValues [in]

A list of the property values.

### -param options [in]

Options for the operation as enumerated by the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmgetfilepropertyoptions">FsrmGetFilePropertyOptions</a> enumeration. The 
      default value is <b>FsrmGetFilePropertyOptions_None</b>.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmgetfilepropertyoptions">FsrmGetFilePropertyOptions</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>