---
UID: NF:fsrm.IFsrmExportImport.ImportFileScreenTemplates
title: IFsrmExportImport::ImportFileScreenTemplates (fsrm.h)
description: Imports one or more file screen templates from the specified file.
helpviewer_keywords: ["FsrmExportImport class [File Server Resource Manager]","ImportFileScreenTemplates method","IFsrmExportImport interface [File Server Resource Manager]","ImportFileScreenTemplates method","IFsrmExportImport.ImportFileScreenTemplates","IFsrmExportImport::ImportFileScreenTemplates","ImportFileScreenTemplates","ImportFileScreenTemplates method [File Server Resource Manager]","ImportFileScreenTemplates method [File Server Resource Manager]","FsrmExportImport class","ImportFileScreenTemplates method [File Server Resource Manager]","IFsrmExportImport interface","fs.ifsrmexportimport_importfilescreentemplates","fsrm.ifsrmexportimport_importfilescreentemplates","fsrm/IFsrmExportImport::ImportFileScreenTemplates"]
old-location: fsrm\ifsrmexportimport_importfilescreentemplates.htm
tech.root: fsrm
ms.assetid: ea2fbd88-777e-454c-8d32-0d704c219558
ms.date: 12/05/2018
ms.keywords: FsrmExportImport class [File Server Resource Manager],ImportFileScreenTemplates method, IFsrmExportImport interface [File Server Resource Manager],ImportFileScreenTemplates method, IFsrmExportImport.ImportFileScreenTemplates, IFsrmExportImport::ImportFileScreenTemplates, ImportFileScreenTemplates, ImportFileScreenTemplates method [File Server Resource Manager], ImportFileScreenTemplates method [File Server Resource Manager],FsrmExportImport class, ImportFileScreenTemplates method [File Server Resource Manager],IFsrmExportImport interface, fs.ifsrmexportimport_importfilescreentemplates, fsrm.ifsrmexportimport_importfilescreentemplates, fsrm/IFsrmExportImport::ImportFileScreenTemplates
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
 - IFsrmExportImport::ImportFileScreenTemplates
 - fsrm/IFsrmExportImport::ImportFileScreenTemplates
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
 - IFsrmExportImport.ImportFileScreenTemplates
 - FsrmExportImport.ImportFileScreenTemplates
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

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface that contains a collection of <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplateimported">IFsrmFileScreenTemplateImported</a> interfaces. To complete the import, you must call the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmFileScreenTemplateImported::Commit</a> method.

## -returns

The method returns the following return values.

## -remarks

You can also use the <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-importtemplates">IFsrmFileScreenTemplateManager::ImportTemplates</a> method to import the templates.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmexportimport">FsrmExportImport</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmexportimport">IFsrmExportImport</a>