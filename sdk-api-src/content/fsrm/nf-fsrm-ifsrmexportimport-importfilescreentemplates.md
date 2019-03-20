---
UID: NF:fsrm.IFsrmExportImport.ImportFileScreenTemplates
title: IFsrmExportImport::ImportFileScreenTemplates (fsrm.h)
author: windows-sdk-content
description: Imports one or more file screen templates from the specified file.
old-location: fsrm\ifsrmexportimport_importfilescreentemplates.htm
tech.root: fsrm
ms.assetid: ea2fbd88-777e-454c-8d32-0d704c219558
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FsrmExportImport class [File Server Resource Manager],ImportFileScreenTemplates method, IFsrmExportImport interface [File Server Resource Manager],ImportFileScreenTemplates method, IFsrmExportImport.ImportFileScreenTemplates, IFsrmExportImport::ImportFileScreenTemplates, ImportFileScreenTemplates, ImportFileScreenTemplates method [File Server Resource Manager], ImportFileScreenTemplates method [File Server Resource Manager],FsrmExportImport class, ImportFileScreenTemplates method [File Server Resource Manager],IFsrmExportImport interface, fs.ifsrmexportimport_importfilescreentemplates, fsrm.ifsrmexportimport_importfilescreentemplates, fsrm/IFsrmExportImport::ImportFileScreenTemplates
ms.topic: method
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmExportImport.ImportFileScreenTemplates
 - FsrmExportImport.ImportFileScreenTemplates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmExportImport::ImportFileScreenTemplates


## -description


Imports one or more file screen templates from the specified file.


## -parameters




### -param filePath [in]

The full path to the file from which to import the file screen templates. The string is limited to 260 characters.


### -param templateNamesSafeArray [in]

A variant that contains the names of the file screen templates to import. Set the variant to empty or <b>NULL</b> to import all templates.

Set the variant type to both <b>VT_ARRAY</b> and <b>VT_VARIANT</b> and the <b>parray</b> member to the <b>SAFEARRAY</b> of <b>BSTR</b>s.


### -param remoteHost [in]

The name of the remote server. To specify the local server, set to an empty string.


### -param templates [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface that contains a collection of <a href="https://msdn.microsoft.com/9e3c3d05-298d-4373-abd2-21de9770e85c">IFsrmFileScreenTemplateImported</a> interfaces. To complete the import, you must call the <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmFileScreenTemplateImported::Commit</a> method.


## -returns



The method returns the following return values.




## -remarks



You can also use the <a href="https://msdn.microsoft.com/0660a1cb-904e-4ed0-bbc8-9903e8848f4e">IFsrmFileScreenTemplateManager::ImportTemplates</a> method to import the templates.




## -see-also




<a href="https://msdn.microsoft.com/ea707982-2d2d-4fb9-a97a-ee5b2a61f8a9">FsrmExportImport</a>



<a href="https://msdn.microsoft.com/5a3b682e-d2c3-43b3-9d10-4bba9d9c81d4">IFsrmExportImport</a>
 

 

