---
UID: NF:fsrm.IFsrmExportImport.ExportFileGroups
title: IFsrmExportImport::ExportFileGroups
author: windows-sdk-content
description: Exports one or more file groups to the specified file.
old-location: fsrm\ifsrmexportimport_exportfilegroups.htm
old-project: Fsrm
ms.assetid: 2be3715f-d9c7-4554-9416-a1cc4e512402
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: ExportFileGroups, ExportFileGroups method [File Server Resource Manager], ExportFileGroups method [File Server Resource Manager],FsrmExportImport class, ExportFileGroups method [File Server Resource Manager],IFsrmExportImport interface, FsrmExportImport class [File Server Resource Manager],ExportFileGroups method, IFsrmExportImport interface [File Server Resource Manager],ExportFileGroups method, IFsrmExportImport.ExportFileGroups, IFsrmExportImport::ExportFileGroups, fs.ifsrmexportimport_exportfilegroups, fsrm.ifsrmexportimport_exportfilegroups, fsrm/IFsrmExportImport::ExportFileGroups
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
 - IFsrmExportImport.ExportFileGroups
 - FsrmExportImport.ExportFileGroups
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
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
    <a href="https://msdn.microsoft.com/7e2c3672-fbb9-4da5-9e20-25c66213843c">IFsrmFileGroupManager::CreateFileGroup</a> 
    method. To enumerate the file groups, call the 
    <a href="https://msdn.microsoft.com/317eb6cf-7bcc-4042-a7b7-05efac84a0c2">IFsrmFileGroupManager::EnumFileGroups</a> 
    method.

You can also use the 
    <a href="https://msdn.microsoft.com/59d7ef32-f06b-4167-8e28-da88da27ab0a">IFsrmFileGroupManager::ExportFileGroups</a> 
    method to export the templates.




## -see-also




<a href="https://msdn.microsoft.com/ea707982-2d2d-4fb9-a97a-ee5b2a61f8a9">FsrmExportImport</a>



<a href="https://msdn.microsoft.com/5a3b682e-d2c3-43b3-9d10-4bba9d9c81d4">IFsrmExportImport</a>
 

 

