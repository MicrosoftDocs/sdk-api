---
UID: NF:fsrm.IFsrmExportImport.ExportFileGroups
title: IFsrmExportImport::ExportFileGroups (fsrm.h)
description: Exports one or more file groups to the specified file.
helpviewer_keywords: ["ExportFileGroups","ExportFileGroups method [File Server Resource Manager]","ExportFileGroups method [File Server Resource Manager]","FsrmExportImport class","ExportFileGroups method [File Server Resource Manager]","IFsrmExportImport interface","FsrmExportImport class [File Server Resource Manager]","ExportFileGroups method","IFsrmExportImport interface [File Server Resource Manager]","ExportFileGroups method","IFsrmExportImport.ExportFileGroups","IFsrmExportImport::ExportFileGroups","fs.ifsrmexportimport_exportfilegroups","fsrm.ifsrmexportimport_exportfilegroups","fsrm/IFsrmExportImport::ExportFileGroups"]
old-location: fsrm\ifsrmexportimport_exportfilegroups.htm
tech.root: fsrm
ms.assetid: 2be3715f-d9c7-4554-9416-a1cc4e512402
ms.date: 12/05/2018
ms.keywords: ExportFileGroups, ExportFileGroups method [File Server Resource Manager], ExportFileGroups method [File Server Resource Manager],FsrmExportImport class, ExportFileGroups method [File Server Resource Manager],IFsrmExportImport interface, FsrmExportImport class [File Server Resource Manager],ExportFileGroups method, IFsrmExportImport interface [File Server Resource Manager],ExportFileGroups method, IFsrmExportImport.ExportFileGroups, IFsrmExportImport::ExportFileGroups, fs.ifsrmexportimport_exportfilegroups, fsrm.ifsrmexportimport_exportfilegroups, fsrm/IFsrmExportImport::ExportFileGroups
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
 - IFsrmExportImport::ExportFileGroups
 - fsrm/IFsrmExportImport::ExportFileGroups
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
 - IFsrmExportImport.ExportFileGroups
 - FsrmExportImport.ExportFileGroups
---

# IFsrmExportImport::ExportFileGroups


## -description

Exports one or more file groups to the specified file.

## -parameters

### -param filePath [in]

The full path to the export file that will contain the file groups in XML format. The string is limited to 
      260 characters.

### -param fileGroupNamesSafeArray [in]

A variant that contains the names of the file groups to export. Set the variant to empty or 
      <b>NULL</b> to export all file groups.

Set the variant type to both 
      <b>VT_ARRAY</b> and <b>VT_VARIANT</b> and the 
      <b>parray</b> member to the <b>SAFEARRAY</b> of 
      <b>BSTR</b>s.

### -param remoteHost [in]

The name of the remote server. To specify the local server, set to an empty string.

## -returns

This method can return the following error codes.

## -remarks

The file group name is specified when you call the 
    <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-createfilegroup">IFsrmFileGroupManager::CreateFileGroup</a> 
    method. To enumerate the file groups, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-enumfilegroups">IFsrmFileGroupManager::EnumFileGroups</a> 
    method.

You can also use the 
    <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-exportfilegroups">IFsrmFileGroupManager::ExportFileGroups</a> 
    method to export the templates.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmexportimport">FsrmExportImport</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmexportimport">IFsrmExportImport</a>