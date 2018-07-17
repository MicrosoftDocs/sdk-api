---
UID: NF:fsrm.IFsrmExportImport.ExportFileScreenTemplates
title: IFsrmExportImport::ExportFileScreenTemplates
author: windows-sdk-content
description: Exports one or more file screen templates to the specified file.
old-location: fsrm\ifsrmexportimport_exportfilescreentemplates.htm
old-project: Fsrm
ms.assetid: 5804dece-7243-4f41-a949-e663852219e8
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ExportFileScreenTemplates, ExportFileScreenTemplates method [File Server Resource Manager], ExportFileScreenTemplates method [File Server Resource Manager],FsrmExportImport class, ExportFileScreenTemplates method [File Server Resource Manager],IFsrmExportImport interface, FsrmExportImport class [File Server Resource Manager],ExportFileScreenTemplates method, IFsrmExportImport interface [File Server Resource Manager],ExportFileScreenTemplates method, IFsrmExportImport.ExportFileScreenTemplates, IFsrmExportImport::ExportFileScreenTemplates, fs.ifsrmexportimport_exportfilescreentemplates, fsrm.ifsrmexportimport_exportfilescreentemplates, fsrm/IFsrmExportImport::ExportFileScreenTemplates
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
 - IFsrmExportImport.ExportFileScreenTemplates
 - FsrmExportImport.ExportFileScreenTemplates
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmExportImport::ExportFileScreenTemplates


## -description


Exports one or more file screen templates to the specified file.


## -parameters




### -param filePath [in]

The full path to the export file that will contain the file screen templates in XML format. The string is limited to 260 characters.


### -param templateNamesSafeArray [in]

A variant that contains the names of the file screen templates to export. Set the variant to empty or <b>NULL</b> to export all templates.

Set the variant type to both <b>VT_ARRAY</b> and <b>VT_VARIANT</b> and the <b>parray</b> member to the <b>SAFEARRAY</b> of <b>BSTR</b>s.


### -param remoteHost [in]

The name of the remote server. To specify the local server, set to an empty string.


## -returns



This method can return the following error codes.




## -remarks



The file screen template name is specified when you call the <a href="https://msdn.microsoft.com/3d654dee-2a27-4dc0-8e2b-fba546abe17e">IFsrmFileScreenTemplateManager::CreateTemplate</a> method. To enumerate the templates, call the <a href="https://msdn.microsoft.com/5bfb82f9-50a5-4266-956d-f99e2982a6a5">IFsrmFileScreenTemplateManager::EnumTemplates</a> method.

You can also use the <a href="https://msdn.microsoft.com/27a0141d-0906-400e-bd5f-81da67a3c501">IFsrmFileScreenTemplateManager::ExportTemplates</a> method to export the templates.




## -see-also




<a href="https://msdn.microsoft.com/ea707982-2d2d-4fb9-a97a-ee5b2a61f8a9">FsrmExportImport</a>



<a href="https://msdn.microsoft.com/5a3b682e-d2c3-43b3-9d10-4bba9d9c81d4">IFsrmExportImport</a>
 

 

