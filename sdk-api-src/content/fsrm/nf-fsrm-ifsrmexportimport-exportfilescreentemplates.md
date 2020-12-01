---
UID: NF:fsrm.IFsrmExportImport.ExportFileScreenTemplates
title: IFsrmExportImport::ExportFileScreenTemplates (fsrm.h)
description: Exports one or more file screen templates to the specified file.
helpviewer_keywords: ["ExportFileScreenTemplates","ExportFileScreenTemplates method [File Server Resource Manager]","ExportFileScreenTemplates method [File Server Resource Manager]","FsrmExportImport class","ExportFileScreenTemplates method [File Server Resource Manager]","IFsrmExportImport interface","FsrmExportImport class [File Server Resource Manager]","ExportFileScreenTemplates method","IFsrmExportImport interface [File Server Resource Manager]","ExportFileScreenTemplates method","IFsrmExportImport.ExportFileScreenTemplates","IFsrmExportImport::ExportFileScreenTemplates","fs.ifsrmexportimport_exportfilescreentemplates","fsrm.ifsrmexportimport_exportfilescreentemplates","fsrm/IFsrmExportImport::ExportFileScreenTemplates"]
old-location: fsrm\ifsrmexportimport_exportfilescreentemplates.htm
tech.root: fsrm
ms.assetid: 5804dece-7243-4f41-a949-e663852219e8
ms.date: 12/05/2018
ms.keywords: ExportFileScreenTemplates, ExportFileScreenTemplates method [File Server Resource Manager], ExportFileScreenTemplates method [File Server Resource Manager],FsrmExportImport class, ExportFileScreenTemplates method [File Server Resource Manager],IFsrmExportImport interface, FsrmExportImport class [File Server Resource Manager],ExportFileScreenTemplates method, IFsrmExportImport interface [File Server Resource Manager],ExportFileScreenTemplates method, IFsrmExportImport.ExportFileScreenTemplates, IFsrmExportImport::ExportFileScreenTemplates, fs.ifsrmexportimport_exportfilescreentemplates, fsrm.ifsrmexportimport_exportfilescreentemplates, fsrm/IFsrmExportImport::ExportFileScreenTemplates
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmExportImport::ExportFileScreenTemplates
 - fsrm/IFsrmExportImport::ExportFileScreenTemplates
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
 - IFsrmExportImport.ExportFileScreenTemplates
 - FsrmExportImport.ExportFileScreenTemplates
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

The file screen template name is specified when you call the <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-createtemplate">IFsrmFileScreenTemplateManager::CreateTemplate</a> method. To enumerate the templates, call the <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-enumtemplates">IFsrmFileScreenTemplateManager::EnumTemplates</a> method.

You can also use the <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-exporttemplates">IFsrmFileScreenTemplateManager::ExportTemplates</a> method to export the templates.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmexportimport">FsrmExportImport</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmexportimport">IFsrmExportImport</a>