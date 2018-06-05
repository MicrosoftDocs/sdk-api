---
UID: NF:fsrm.IFsrmExportImport.ExportQuotaTemplates
title: IFsrmExportImport::ExportQuotaTemplates
author: windows-sdk-content
description: Exports one or more quota templates to the specified file.
old-location: fsrm\ifsrmexportimport_exportquotatemplates.htm
old-project: Fsrm
ms.assetid: ede839ed-3e6f-4b70-bede-07e097ecc1e6
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: ExportQuotaTemplates, ExportQuotaTemplates method [File Server Resource Manager], ExportQuotaTemplates method [File Server Resource Manager],FsrmExportImport class, ExportQuotaTemplates method [File Server Resource Manager],IFsrmExportImport interface, FsrmExportImport class [File Server Resource Manager],ExportQuotaTemplates method, IFsrmExportImport interface [File Server Resource Manager],ExportQuotaTemplates method, IFsrmExportImport.ExportQuotaTemplates, IFsrmExportImport::ExportQuotaTemplates, fs.ifsrmexportimport_exportquotatemplates, fsrm.ifsrmexportimport_exportquotatemplates, fsrm/IFsrmExportImport::ExportQuotaTemplates
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmExportImport.ExportQuotaTemplates
-	FsrmExportImport.ExportQuotaTemplates
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmExportImport::ExportQuotaTemplates


## -description


Exports one or more quota templates to the specified file.


## -parameters




### -param filePath [in]

The full path to the export file that will contain the quota templates in XML format. The string is limited 
      to 260 characters.


### -param templateNamesSafeArray [in]

A variant that contains the names of the quota templates to export. Set the variant to empty or 
       <b>NULL</b> to export all templates.

Set the variant type to both <b>VT_ARRAY</b> and <b>VT_VARIANT</b> and 
       the <b>parray</b> member to the <b>SAFEARRAY</b> of 
       <b>BSTR</b>s.


### -param remoteHost [in]

The name of the remote server. To specify the local server, set to an empty string.


## -returns



This method can return the following error codes.




## -remarks



The quota template name is specified when you call the 
    <a href="https://msdn.microsoft.com/d8dbc0fb-de02-4491-94f5-e845a2338251">IFsrmQuotaTemplateManager::CreateTemplate</a> 
    method. To enumerate the templates, call the 
    <a href="https://msdn.microsoft.com/e5f5b94a-6b17-4379-9141-07ec70a830e9">IFsrmQuotaTemplateManager::EnumTemplates</a> 
    method.

You can also use the 
    <a href="https://msdn.microsoft.com/36ba071b-4db2-42fb-90a8-838c45dfdd16">IFsrmQuotaTemplateManager::ExportTemplates</a> 
    method to export the templates.




## -see-also




<a href="https://msdn.microsoft.com/ea707982-2d2d-4fb9-a97a-ee5b2a61f8a9">FsrmExportImport</a>



<a href="https://msdn.microsoft.com/5a3b682e-d2c3-43b3-9d10-4bba9d9c81d4">IFsrmExportImport</a>
 

 

