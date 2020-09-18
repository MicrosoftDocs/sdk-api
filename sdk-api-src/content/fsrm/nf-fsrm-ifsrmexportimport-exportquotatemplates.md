---
UID: NF:fsrm.IFsrmExportImport.ExportQuotaTemplates
title: IFsrmExportImport::ExportQuotaTemplates (fsrm.h)
description: Exports one or more quota templates to the specified file.
helpviewer_keywords: ["ExportQuotaTemplates","ExportQuotaTemplates method [File Server Resource Manager]","ExportQuotaTemplates method [File Server Resource Manager]","FsrmExportImport class","ExportQuotaTemplates method [File Server Resource Manager]","IFsrmExportImport interface","FsrmExportImport class [File Server Resource Manager]","ExportQuotaTemplates method","IFsrmExportImport interface [File Server Resource Manager]","ExportQuotaTemplates method","IFsrmExportImport.ExportQuotaTemplates","IFsrmExportImport::ExportQuotaTemplates","fs.ifsrmexportimport_exportquotatemplates","fsrm.ifsrmexportimport_exportquotatemplates","fsrm/IFsrmExportImport::ExportQuotaTemplates"]
old-location: fsrm\ifsrmexportimport_exportquotatemplates.htm
tech.root: fsrm
ms.assetid: ede839ed-3e6f-4b70-bede-07e097ecc1e6
ms.date: 12/05/2018
ms.keywords: ExportQuotaTemplates, ExportQuotaTemplates method [File Server Resource Manager], ExportQuotaTemplates method [File Server Resource Manager],FsrmExportImport class, ExportQuotaTemplates method [File Server Resource Manager],IFsrmExportImport interface, FsrmExportImport class [File Server Resource Manager],ExportQuotaTemplates method, IFsrmExportImport interface [File Server Resource Manager],ExportQuotaTemplates method, IFsrmExportImport.ExportQuotaTemplates, IFsrmExportImport::ExportQuotaTemplates, fs.ifsrmexportimport_exportquotatemplates, fsrm.ifsrmexportimport_exportquotatemplates, fsrm/IFsrmExportImport::ExportQuotaTemplates
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
 - IFsrmExportImport::ExportQuotaTemplates
 - fsrm/IFsrmExportImport::ExportQuotaTemplates
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
 - IFsrmExportImport.ExportQuotaTemplates
 - FsrmExportImport.ExportQuotaTemplates
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
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-createtemplate">IFsrmQuotaTemplateManager::CreateTemplate</a> 
    method. To enumerate the templates, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-enumtemplates">IFsrmQuotaTemplateManager::EnumTemplates</a> 
    method.

You can also use the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-exporttemplates">IFsrmQuotaTemplateManager::ExportTemplates</a> 
    method to export the templates.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmexportimport">FsrmExportImport</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmexportimport">IFsrmExportImport</a>