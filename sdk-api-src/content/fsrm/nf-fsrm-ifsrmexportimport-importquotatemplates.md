---
UID: NF:fsrm.IFsrmExportImport.ImportQuotaTemplates
title: IFsrmExportImport::ImportQuotaTemplates (fsrm.h)
description: Imports one or more quota templates from the specified file.
helpviewer_keywords: ["FsrmExportImport class [File Server Resource Manager]","ImportQuotaTemplates method","IFsrmExportImport interface [File Server Resource Manager]","ImportQuotaTemplates method","IFsrmExportImport.ImportQuotaTemplates","IFsrmExportImport::ImportQuotaTemplates","ImportQuotaTemplates","ImportQuotaTemplates method [File Server Resource Manager]","ImportQuotaTemplates method [File Server Resource Manager]","FsrmExportImport class","ImportQuotaTemplates method [File Server Resource Manager]","IFsrmExportImport interface","fs.ifsrmexportimport_importquotatemplates","fsrm.ifsrmexportimport_importquotatemplates","fsrm/IFsrmExportImport::ImportQuotaTemplates"]
old-location: fsrm\ifsrmexportimport_importquotatemplates.htm
tech.root: fsrm
ms.assetid: 90b70f64-fbc7-48d2-9cf7-71e625ed32af
ms.date: 12/05/2018
ms.keywords: FsrmExportImport class [File Server Resource Manager],ImportQuotaTemplates method, IFsrmExportImport interface [File Server Resource Manager],ImportQuotaTemplates method, IFsrmExportImport.ImportQuotaTemplates, IFsrmExportImport::ImportQuotaTemplates, ImportQuotaTemplates, ImportQuotaTemplates method [File Server Resource Manager], ImportQuotaTemplates method [File Server Resource Manager],FsrmExportImport class, ImportQuotaTemplates method [File Server Resource Manager],IFsrmExportImport interface, fs.ifsrmexportimport_importquotatemplates, fsrm.ifsrmexportimport_importquotatemplates, fsrm/IFsrmExportImport::ImportQuotaTemplates
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
 - IFsrmExportImport::ImportQuotaTemplates
 - fsrm/IFsrmExportImport::ImportQuotaTemplates
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
 - IFsrmExportImport.ImportQuotaTemplates
 - FsrmExportImport.ImportQuotaTemplates
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

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface that contains a collection of <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotatemplateimported">IFsrmQuotaTemplateImported</a> interfaces. To complete the import, you must call the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmQuotaTemplateImported::Commit</a> method.

## -returns

The method returns the following return values.

## -remarks

You can also use the <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-importtemplates">IFsrmQuotaTemplateManager::ImportTemplates</a> method to import the templates.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmexportimport">FsrmExportImport</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmexportimport">IFsrmExportImport</a>