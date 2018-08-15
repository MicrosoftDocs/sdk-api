---
UID: NE:fsrmenums._FsrmReportLimit
title: "_FsrmReportLimit"
author: windows-sdk-content
description: Defines the limit used to limit the files included in a report.
old-location: fsrm\fsrmreportlimit.htm
old-project: fsrm
ms.assetid: 225c583c-679c-43b4-85f4-3f2294fa7bc3
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: FsrmReportLimit, FsrmReportLimit enumeration [File Server Resource Manager], FsrmReportLimit_MaxDuplicateGroups, FsrmReportLimit_MaxFileGroups, FsrmReportLimit_MaxFileScreenEvents, FsrmReportLimit_MaxFiles, FsrmReportLimit_MaxFilesPerDuplGroup, FsrmReportLimit_MaxFilesPerFileGroup, FsrmReportLimit_MaxFilesPerOwner, FsrmReportLimit_MaxFilesPerPropertyValue, FsrmReportLimit_MaxFolders, FsrmReportLimit_MaxOwners, FsrmReportLimit_MaxPropertyValues, FsrmReportLimit_MaxQuotas, _FsrmReportLimit, fs.fsrmreportlimit, fsrm.fsrmreportlimit, fsrmenums/FsrmReportLimit, fsrmenums/FsrmReportLimit_MaxDuplicateGroups, fsrmenums/FsrmReportLimit_MaxFileGroups, fsrmenums/FsrmReportLimit_MaxFileScreenEvents, fsrmenums/FsrmReportLimit_MaxFiles, fsrmenums/FsrmReportLimit_MaxFilesPerDuplGroup, fsrmenums/FsrmReportLimit_MaxFilesPerFileGroup, fsrmenums/FsrmReportLimit_MaxFilesPerOwner, fsrmenums/FsrmReportLimit_MaxFilesPerPropertyValue, fsrmenums/FsrmReportLimit_MaxFolders, fsrmenums/FsrmReportLimit_MaxOwners, fsrmenums/FsrmReportLimit_MaxPropertyValues, fsrmenums/FsrmReportLimit_MaxQuotas
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmEnums.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FsrmReportLimit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmReportLimit
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# _FsrmReportLimit enumeration


## -description


Defines the limit used to limit the files included in a report.


## -enum-fields




### -field FsrmReportLimit_MaxFiles

The report will list up to a maximum number of files. Applies to all report types.


### -field FsrmReportLimit_MaxFileGroups

A <b>FsrmReportType_FilesByType</b> report will list up to a maximum number of file 
      groups.


### -field FsrmReportLimit_MaxOwners

A <b>FsrmReportType_FilesByOwner</b> report will list up to a maximum number of 
      owners.


### -field FsrmReportLimit_MaxFilesPerFileGroup

A <b>FsrmReportType_FilesByProperty</b> report will list up to a maximum number of 
      files per file group.


### -field FsrmReportLimit_MaxFilesPerOwner

A <b>FsrmReportType_FilesByOwner</b> report will be limited to a maximum number of 
      files per owner.


### -field FsrmReportLimit_MaxFilesPerDuplGroup

A <b>FsrmReportType_DuplicateFiles</b> report will list up to a maximum number of 
      files per duplicated file group.


### -field FsrmReportLimit_MaxDuplicateGroups

A <b>FsrmReportType_DuplicateFiles</b> report will list up to a maximum number of 
      duplicated file groups.


### -field FsrmReportLimit_MaxQuotas

A <b>FsrmReportType_QuotaUsage</b> report will list up to a maximum number of 
      quotas.


### -field FsrmReportLimit_MaxFileScreenEvents

A <b>FsrmReportType_FileScreenAudit</b> report will list up to a maximum number of 
      file screen events.


### -field FsrmReportLimit_MaxPropertyValues

A <b>FsrmReportType_FilesByProperty</b> report will list up to a maximum number of 
      property values.


### -field FsrmReportLimit_MaxFilesPerPropertyValue

A <b>FsrmReportType_FilesByProperty</b> report will list up to a maximum number of 
      files per property value.


### -field FsrmReportLimit_MaxFolders

A <b>FsrmReportType_FolderByProperty</b> report will list up to a maximum number of 
       folders.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This report limit is not supported before Windows Server 2012.


## -remarks



You specify the  value for the limit in the <i>limitValue</i> parameter when calling the 
    <a href="https://msdn.microsoft.com/7d5a73ab-eccb-42e5-8796-d2986deccd34">IFsrmReportManager::SetReportSizeLimit</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/6fb5cb02-371b-4d07-9f13-d0409d5835d4">FsrmReportType</a>



<a href="https://msdn.microsoft.com/1fe2546c-d70c-466a-8640-77cc2403a91d">IFsrmReportManager::GetReportSizeLimit</a>



<a href="https://msdn.microsoft.com/7d5a73ab-eccb-42e5-8796-d2986deccd34">IFsrmReportManager::SetReportSizeLimit</a>
 

 

