---
UID: NF:fsrmpipeline.IFsrmPropertyBag.get_RelativePath
title: IFsrmPropertyBag::get_RelativePath
author: windows-sdk-content
description: The relative path to the file.
old-location: fsrm\ifsrmpropertybag_relativepath.htm
old-project: Fsrm
ms.assetid: 4304228a-5e8e-4e2d-9fc9-48777cb23251
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmPropertyBag interface [File Server Resource Manager],RelativePath property, IFsrmPropertyBag.RelativePath, IFsrmPropertyBag.get_RelativePath, IFsrmPropertyBag::RelativePath, IFsrmPropertyBag::get_RelativePath, RelativePath property [File Server Resource Manager], RelativePath property [File Server Resource Manager],IFsrmPropertyBag interface, fs.ifsrmpropertybag_relativepath, fsrm.ifsrmpropertybag_relativepath, fsrmpipeline/IFsrmPropertyBag::RelativePath, fsrmpipeline/IFsrmPropertyBag::get_RelativePath, get_RelativePath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmPropertyBag.RelativePath
-	IFsrmPropertyBag.get_RelativePath
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmPropertyBag::get_RelativePath


## -description


The relative path to the file.

This property is read-only.


## -parameters


## -remarks



The relative path is the path of the file relative to the volume root.  For example, if the path to the file is "P:\folder1\subfolderA\test.txt", the relative path would be "\folder1\subfolderA".

The caller should not expect that the relative path returned will consistently have leading or trailing backslashes.




## -see-also




<a href="https://msdn.microsoft.com/237f024d-2b1d-45d5-a63d-c530426278e6">IFsrmPropertyBag</a>
 

 

