---
UID: NE:fsrmenums._FsrmReportLimit
title: FsrmReportLimit (fsrmenums.h)
description: Defines the limit used to limit the files included in a report.
helpviewer_keywords: ["FsrmReportLimit","FsrmReportLimit enumeration [File Server Resource Manager]","FsrmReportLimit_MaxDuplicateGroups","FsrmReportLimit_MaxFileGroups","FsrmReportLimit_MaxFileScreenEvents","FsrmReportLimit_MaxFiles","FsrmReportLimit_MaxFilesPerDuplGroup","FsrmReportLimit_MaxFilesPerFileGroup","FsrmReportLimit_MaxFilesPerOwner","FsrmReportLimit_MaxFilesPerPropertyValue","FsrmReportLimit_MaxFolders","FsrmReportLimit_MaxOwners","FsrmReportLimit_MaxPropertyValues","FsrmReportLimit_MaxQuotas","fs.fsrmreportlimit","fsrm.fsrmreportlimit","fsrmenums/FsrmReportLimit","fsrmenums/FsrmReportLimit_MaxDuplicateGroups","fsrmenums/FsrmReportLimit_MaxFileGroups","fsrmenums/FsrmReportLimit_MaxFileScreenEvents","fsrmenums/FsrmReportLimit_MaxFiles","fsrmenums/FsrmReportLimit_MaxFilesPerDuplGroup","fsrmenums/FsrmReportLimit_MaxFilesPerFileGroup","fsrmenums/FsrmReportLimit_MaxFilesPerOwner","fsrmenums/FsrmReportLimit_MaxFilesPerPropertyValue","fsrmenums/FsrmReportLimit_MaxFolders","fsrmenums/FsrmReportLimit_MaxOwners","fsrmenums/FsrmReportLimit_MaxPropertyValues","fsrmenums/FsrmReportLimit_MaxQuotas"]
old-location: fsrm\fsrmreportlimit.htm
tech.root: fsrm
ms.assetid: 225c583c-679c-43b4-85f4-3f2294fa7bc3
ms.date: 12/05/2018
ms.keywords: FsrmReportLimit, FsrmReportLimit enumeration [File Server Resource Manager], FsrmReportLimit_MaxDuplicateGroups, FsrmReportLimit_MaxFileGroups, FsrmReportLimit_MaxFileScreenEvents, FsrmReportLimit_MaxFiles, FsrmReportLimit_MaxFilesPerDuplGroup, FsrmReportLimit_MaxFilesPerFileGroup, FsrmReportLimit_MaxFilesPerOwner, FsrmReportLimit_MaxFilesPerPropertyValue, FsrmReportLimit_MaxFolders, FsrmReportLimit_MaxOwners, FsrmReportLimit_MaxPropertyValues, FsrmReportLimit_MaxQuotas, fs.fsrmreportlimit, fsrm.fsrmreportlimit, fsrmenums/FsrmReportLimit, fsrmenums/FsrmReportLimit_MaxDuplicateGroups, fsrmenums/FsrmReportLimit_MaxFileGroups, fsrmenums/FsrmReportLimit_MaxFileScreenEvents, fsrmenums/FsrmReportLimit_MaxFiles, fsrmenums/FsrmReportLimit_MaxFilesPerDuplGroup, fsrmenums/FsrmReportLimit_MaxFilesPerFileGroup, fsrmenums/FsrmReportLimit_MaxFilesPerOwner, fsrmenums/FsrmReportLimit_MaxFilesPerPropertyValue, fsrmenums/FsrmReportLimit_MaxFolders, fsrmenums/FsrmReportLimit_MaxOwners, fsrmenums/FsrmReportLimit_MaxPropertyValues, fsrmenums/FsrmReportLimit_MaxQuotas
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FsrmReportLimit
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmReportLimit
 - fsrmenums/_FsrmReportLimit
 - FsrmReportLimit
 - fsrmenums/FsrmReportLimit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmReportLimit
---

# FsrmReportLimit enumeration


## -description

Defines the limit used to limit the files included in a report.

## -enum-fields

### -field FsrmReportLimit_MaxFiles:1

The report will list up to a maximum number of files. Applies to all report types.

### -field FsrmReportLimit_MaxFileGroups:2

A <b>FsrmReportType_FilesByType</b> report will list up to a maximum number of file 
      groups.

### -field FsrmReportLimit_MaxOwners:3

A <b>FsrmReportType_FilesByOwner</b> report will list up to a maximum number of 
      owners.

### -field FsrmReportLimit_MaxFilesPerFileGroup:4

A <b>FsrmReportType_FilesByProperty</b> report will list up to a maximum number of 
      files per file group.

### -field FsrmReportLimit_MaxFilesPerOwner:5

A <b>FsrmReportType_FilesByOwner</b> report will be limited to a maximum number of 
      files per owner.

### -field FsrmReportLimit_MaxFilesPerDuplGroup:6

A <b>FsrmReportType_DuplicateFiles</b> report will list up to a maximum number of 
      files per duplicated file group.

### -field FsrmReportLimit_MaxDuplicateGroups:7

A <b>FsrmReportType_DuplicateFiles</b> report will list up to a maximum number of 
      duplicated file groups.

### -field FsrmReportLimit_MaxQuotas:8

A <b>FsrmReportType_QuotaUsage</b> report will list up to a maximum number of 
      quotas.

### -field FsrmReportLimit_MaxFileScreenEvents:9

A <b>FsrmReportType_FileScreenAudit</b> report will list up to a maximum number of 
      file screen events.

### -field FsrmReportLimit_MaxPropertyValues:10

A <b>FsrmReportType_FilesByProperty</b> report will list up to a maximum number of 
      property values.

### -field FsrmReportLimit_MaxFilesPerPropertyValue:11

A <b>FsrmReportType_FilesByProperty</b> report will list up to a maximum number of 
      files per property value.

### -field FsrmReportLimit_MaxFolders:12

A <b>FsrmReportType_FolderByProperty</b> report will list up to a maximum number of 
       folders.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This report limit is not supported before Windows Server 2012.

## -remarks

You specify the  value for the limit in the <i>limitValue</i> parameter when calling the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setreportsizelimit">IFsrmReportManager::SetReportSizeLimit</a> 
    method.

## -see-also

<a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreporttype">FsrmReportType</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-getreportsizelimit">IFsrmReportManager::GetReportSizeLimit</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setreportsizelimit">IFsrmReportManager::SetReportSizeLimit</a>
