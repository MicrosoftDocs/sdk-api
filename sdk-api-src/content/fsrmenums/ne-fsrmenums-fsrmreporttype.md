---
UID: NE:fsrmenums._FsrmReportType
title: FsrmReportType (fsrmenums.h)
description: Defines the types of reports that you can generate.
helpviewer_keywords: ["FsrmReportType","FsrmReportType enumeration [File Server Resource Manager]","FsrmReportType_AutomaticClassification","FsrmReportType_DuplicateFiles","FsrmReportType_Expiration","FsrmReportType_ExportReport","FsrmReportType_FileScreenAudit","FsrmReportType_FilesByOwner","FsrmReportType_FilesByProperty","FsrmReportType_FilesByType","FsrmReportType_FoldersByProperty","FsrmReportType_LargeFiles","FsrmReportType_LeastRecentlyAccessed","FsrmReportType_MostRecentlyAccessed","FsrmReportType_QuotaUsage","FsrmReportType_Unknown","fs.fsrmreporttype","fsrm.fsrmreporttype","fsrmenums/FsrmReportType","fsrmenums/FsrmReportType_AutomaticClassification","fsrmenums/FsrmReportType_DuplicateFiles","fsrmenums/FsrmReportType_Expiration","fsrmenums/FsrmReportType_ExportReport","fsrmenums/FsrmReportType_FileScreenAudit","fsrmenums/FsrmReportType_FilesByOwner","fsrmenums/FsrmReportType_FilesByProperty","fsrmenums/FsrmReportType_FilesByType","fsrmenums/FsrmReportType_FoldersByProperty","fsrmenums/FsrmReportType_LargeFiles","fsrmenums/FsrmReportType_LeastRecentlyAccessed","fsrmenums/FsrmReportType_MostRecentlyAccessed","fsrmenums/FsrmReportType_QuotaUsage","fsrmenums/FsrmReportType_Unknown"]
old-location: fsrm\fsrmreporttype.htm
tech.root: fsrm
ms.assetid: 6fb5cb02-371b-4d07-9f13-d0409d5835d4
ms.date: 12/05/2018
ms.keywords: FsrmReportType, FsrmReportType enumeration [File Server Resource Manager], FsrmReportType_AutomaticClassification, FsrmReportType_DuplicateFiles, FsrmReportType_Expiration, FsrmReportType_ExportReport, FsrmReportType_FileScreenAudit, FsrmReportType_FilesByOwner, FsrmReportType_FilesByProperty, FsrmReportType_FilesByType, FsrmReportType_FoldersByProperty, FsrmReportType_LargeFiles, FsrmReportType_LeastRecentlyAccessed, FsrmReportType_MostRecentlyAccessed, FsrmReportType_QuotaUsage, FsrmReportType_Unknown, fs.fsrmreporttype, fsrm.fsrmreporttype, fsrmenums/FsrmReportType, fsrmenums/FsrmReportType_AutomaticClassification, fsrmenums/FsrmReportType_DuplicateFiles, fsrmenums/FsrmReportType_Expiration, fsrmenums/FsrmReportType_ExportReport, fsrmenums/FsrmReportType_FileScreenAudit, fsrmenums/FsrmReportType_FilesByOwner, fsrmenums/FsrmReportType_FilesByProperty, fsrmenums/FsrmReportType_FilesByType, fsrmenums/FsrmReportType_FoldersByProperty, fsrmenums/FsrmReportType_LargeFiles, fsrmenums/FsrmReportType_LeastRecentlyAccessed, fsrmenums/FsrmReportType_MostRecentlyAccessed, fsrmenums/FsrmReportType_QuotaUsage, fsrmenums/FsrmReportType_Unknown
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
req.typenames: FsrmReportType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmReportType
 - fsrmenums/_FsrmReportType
 - FsrmReportType
 - fsrmenums/FsrmReportType
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
 - FsrmReportType
---

# FsrmReportType enumeration


## -description

Defines the types of reports that you can generate.

## -enum-fields

### -field FsrmReportType_Unknown:0

The report type is unknown. Do not use this flag.

### -field FsrmReportType_LargeFiles:1

Lists files that are larger than a specified size. Set the filter value to the size, in bytes.

### -field FsrmReportType_FilesByType:2

Lists groups of files. Create a file group and use file name patterns to specify the members of the group. 
      Set the filter value to the name of the file group.

### -field FsrmReportType_LeastRecentlyAccessed:3

Lists files that have not been accessed in the last <i>n</i> days. Specify the filter 
      value in days.

### -field FsrmReportType_MostRecentlyAccessed:4

Lists files that have been accessed in the last <i>n</i> days. Specify the filter value 
      in days.

### -field FsrmReportType_QuotaUsage:5

Lists quotas that exceed the specified threshold. Set the filter value to the threshold.

### -field FsrmReportType_FilesByOwner:6

Lists files grouped by their owner. Set the filter value to the list of owners whose files you want 
      included in the report.

### -field FsrmReportType_ExportReport:7

Lists all files in the scope of the report job; there is no filtering. You can specify the XML or CSV file 
       formats only for this report type. This report cannot be sent through email.

For an action report, the scope is based on the quota or file screen event that initiated the report.

### -field FsrmReportType_DuplicateFiles:8

Lists duplicate files. All files with the same file name, file size, and last modify time under the scope 
      of the report job are considered duplicates. For example, if the scope of the report is C:\ and 
      D:\ and file file1.txt exists in C:&#92;<i>folder1</i>\, 
      C:&#92;<i>folder2</i>\ and D:&#92;<i>folder1</i>\ with 
      the same modify time and file size, then the files are considered duplicates.

### -field FsrmReportType_FileScreenAudit:9

Lists file screening events that have occurred.

### -field FsrmReportType_FilesByProperty:10

Lists files, grouped by property value, that contain the specified property (you can specify only one 
       property on which to report).

<b>Windows Server 2008:  </b>This report type is not supported before Windows Server 2008 R2.

### -field FsrmReportType_AutomaticClassification:11

For internal use only; do not specify.

<b>Windows Server 2008:  </b>This report type is not supported before Windows Server 2008 R2.

### -field FsrmReportType_Expiration:12

For internal use only; do not specify.

<b>Windows Server 2008:  </b>This report type is not supported before Windows Server 2008 R2.

### -field FsrmReportType_FoldersByProperty:13

Lists folders, grouped by property value, that contain the specified property (you can specify only one 
       property on which to report).

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This report type is not supported before Windows Server 2012.

## -remarks

To specify the values for report types that require a filter (for example, listing files over a specified 
    size), call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setdefaultfilter">IFsrmReportManager::SetDefaultFilter</a> 
    method.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactionreport-get_reporttypes">IFsrmActionReport::ReportTypes</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreport-get_type">IFsrmReport::Type</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportjob-createreport">IFsrmReportJob::CreateReportCreateReport</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-getdefaultfilter">IFsrmReportManager::GetDefaultFilter</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-isfiltervalidforreporttype">IFsrmReportManager::IsFilterValidForReportType</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setdefaultfilter">IFsrmReportManager::SetDefaultFilter</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>
