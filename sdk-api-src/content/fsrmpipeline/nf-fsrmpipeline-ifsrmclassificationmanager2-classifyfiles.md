---
UID: NF:fsrmpipeline.IFsrmClassificationManager2.ClassifyFiles
title: IFsrmClassificationManager2::ClassifyFiles
author: windows-sdk-content
description: This method is used to perform bulk enumeration, setting, and clearing of file properties.
old-location: fsrm\ifsrmclassificationmanager2_classifyfiles.htm
old-project: Fsrm
ms.assetid: 1dee9185-f83c-4e49-bf29-143271445046
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ClassifyFiles, ClassifyFiles method [File Server Resource Manager], ClassifyFiles method [File Server Resource Manager],FsrmClassificationManager class, ClassifyFiles method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],ClassifyFiles method, IFsrmClassificationManager2 interface [File Server Resource Manager],ClassifyFiles method, IFsrmClassificationManager2.ClassifyFiles, IFsrmClassificationManager2::ClassifyFiles, fs.ifsrmclassificationmanager2_classifyfiles, fsrm.ifsrmclassificationmanager2_classifyfiles, fsrmpipeline/IFsrmClassificationManager2::ClassifyFiles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
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
      <a href="https://msdn.microsoft.com/d909e244-344f-4da9-987c-de406c2dc359">FsrmGetFilePropertyOptions</a> enumeration. The 
      default value is <b>FsrmGetFilePropertyOptions_None</b>.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/d909e244-344f-4da9-987c-de406c2dc359">FsrmGetFilePropertyOptions</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

