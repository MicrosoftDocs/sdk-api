---
UID: NF:fsrm.IFsrmExportImport.ImportQuotaTemplates
title: IFsrmExportImport::ImportQuotaTemplates
author: windows-sdk-content
description: Imports one or more quota templates from the specified file.
old-location: fsrm\ifsrmexportimport_importquotatemplates.htm
old-project: fsrm
ms.assetid: 90b70f64-fbc7-48d2-9cf7-71e625ed32af
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: FsrmExportImport class [File Server Resource Manager],ImportQuotaTemplates method, IFsrmExportImport interface [File Server Resource Manager],ImportQuotaTemplates method, IFsrmExportImport.ImportQuotaTemplates, IFsrmExportImport::ImportQuotaTemplates, ImportQuotaTemplates, ImportQuotaTemplates method [File Server Resource Manager], ImportQuotaTemplates method [File Server Resource Manager],FsrmExportImport class, ImportQuotaTemplates method [File Server Resource Manager],IFsrmExportImport interface, fs.ifsrmexportimport_importquotatemplates, fsrm.ifsrmexportimport_importquotatemplates, fsrm/IFsrmExportImport::ImportQuotaTemplates
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmExportImport.ImportQuotaTemplates
 - FsrmExportImport.ImportQuotaTemplates
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmExportImport::ImportQuotaTemplates


## -description


Imports one or more quota templates from the specified file.


## -parameters




### -param filePath [in]

The full path to the file from which to import the quota templates. The string is limited to 260 characters.


### -param templateNamesSafeArray [in]

A variant that contains the names of the quota templates to import. Set the variant to empty or <b>NULL</b> to import all templates.

Set the variant type to both <b>VT_ARRAY</b> and <b>VT_VARIANT</b> and the <b>parray</b> member to the <b>SAFEARRAY</b> of <b>BSTR</b>s.


### -param remoteHost [in]

The name of the remote server. To specify the local server, set to an empty string.


### -param templates [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface that contains a collection of <a href="https://msdn.microsoft.com/0349a772-9862-4131-b3be-96eec8e41b01">IFsrmQuotaTemplateImported</a> interfaces. To complete the import, you must call the <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmQuotaTemplateImported::Commit</a> method.


## -returns



The method returns the following return values.




## -remarks



You can also use the <a href="https://msdn.microsoft.com/f530d7fc-8b41-4a5e-a10a-b9211c7fe2bb">IFsrmQuotaTemplateManager::ImportTemplates</a> method to import the templates.




## -see-also




<a href="https://msdn.microsoft.com/ea707982-2d2d-4fb9-a97a-ee5b2a61f8a9">FsrmExportImport</a>



<a href="https://msdn.microsoft.com/5a3b682e-d2c3-43b3-9d10-4bba9d9c81d4">IFsrmExportImport</a>
 

 

