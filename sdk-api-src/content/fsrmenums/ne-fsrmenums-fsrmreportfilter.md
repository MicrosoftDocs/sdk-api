---
UID: NE:fsrmenums._FsrmReportFilter
title: FsrmReportFilter (fsrmenums.h)
description: Defines the filters that you can use to limit the files that are included in a report.
helpviewer_keywords: ["FsrmReportFilter","FsrmReportFilter enumeration [File Server Resource Manager]","FsrmReportFilter_FileGroups","FsrmReportFilter_MaxAgeDays","FsrmReportFilter_MinAgeDays","FsrmReportFilter_MinQuotaUsage","FsrmReportFilter_MinSize","FsrmReportFilter_NamePattern","FsrmReportFilter_Owners","FsrmReportFilter_Property","fs.fsrmreportfilter","fsrm.fsrmreportfilter","fsrmenums/FsrmReportFilter","fsrmenums/FsrmReportFilter_FileGroups","fsrmenums/FsrmReportFilter_MaxAgeDays","fsrmenums/FsrmReportFilter_MinAgeDays","fsrmenums/FsrmReportFilter_MinQuotaUsage","fsrmenums/FsrmReportFilter_MinSize","fsrmenums/FsrmReportFilter_NamePattern","fsrmenums/FsrmReportFilter_Owners","fsrmenums/FsrmReportFilter_Property"]
old-location: fsrm\fsrmreportfilter.htm
tech.root: fsrm
ms.assetid: 6f38ec9a-8876-44ce-9d44-f3982f1880ca
ms.date: 12/05/2018
ms.keywords: FsrmReportFilter, FsrmReportFilter enumeration [File Server Resource Manager], FsrmReportFilter_FileGroups, FsrmReportFilter_MaxAgeDays, FsrmReportFilter_MinAgeDays, FsrmReportFilter_MinQuotaUsage, FsrmReportFilter_MinSize, FsrmReportFilter_NamePattern, FsrmReportFilter_Owners, FsrmReportFilter_Property, fs.fsrmreportfilter, fsrm.fsrmreportfilter, fsrmenums/FsrmReportFilter, fsrmenums/FsrmReportFilter_FileGroups, fsrmenums/FsrmReportFilter_MaxAgeDays, fsrmenums/FsrmReportFilter_MinAgeDays, fsrmenums/FsrmReportFilter_MinQuotaUsage, fsrmenums/FsrmReportFilter_MinSize, fsrmenums/FsrmReportFilter_NamePattern, fsrmenums/FsrmReportFilter_Owners, fsrmenums/FsrmReportFilter_Property
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
req.typenames: FsrmReportFilter
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmReportFilter
 - fsrmenums/_FsrmReportFilter
 - FsrmReportFilter
 - fsrmenums/FsrmReportFilter
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
 - FsrmReportFilter
---

# FsrmReportFilter enumeration


## -description

Defines the filters that you can use to limit the files that are included in a report.

## -enum-fields

### -field FsrmReportFilter_MinSize:1

The report will show only files that meet a minimum size.

Applies to the <b>FsrmReportType_LargeFiles</b> report type.

### -field FsrmReportFilter_MinAgeDays:2

The report will show only files that were accessed more than a minimum number of days ago.

Applies to the <b>FsrmReportType_LeastRecentlyAccessed</b> and 
       <b>FsrmReportType_FileScreenAudit</b> report types.

### -field FsrmReportFilter_MaxAgeDays:3

The report will show only files that were accessed prior to a maximum number of days ago.

Applies to the <b>FsrmReportType_MostRecentlyAccessed</b> report type.

### -field FsrmReportFilter_MinQuotaUsage:4

The report will show only quotas that meet a certain disk space usage level.

Applies to the <b>FsrmReportType_QuotaUsage</b> report type.

### -field FsrmReportFilter_FileGroups:5

The report will show only files from a specified set of file groups.

Applies to the <b>FsrmReportType_FilesByType</b> report type.

### -field FsrmReportFilter_Owners:6

The report will show only files that belong to specified owners. The format of the owner string can be either 
       the user principal name 
       ("<i>UserName</i>@<i>Domain</i>" or 
       "<i>Domain</i>&#92;<i>UserName</i>") or a SID in string 
       format.

Applies to the <b>FsrmReportType_FilesByOwner</b> report type.

### -field FsrmReportFilter_NamePattern:7

The report will show only files with names that match the specified pattern.

Applies to the <b>FsrmReportType_LargeFiles</b>, 
       <b>FsrmReportType_MostRecentlyAccessed</b>, 
       <b>FsrmReportType_LeastRecentlyAccessed</b>, 
       <b>FsrmReportType_FilesByOwner</b>, and  
       <b>FsrmReportType_FilesByProperty</b> report types. For these report types, multiple 
       filters could exist. For example, for the <b>FsrmReportType_LargeFiles</b> report type, 
       both the <b>FsrmReportFilter_MinSize</b> and 
       <b>FsrmReportFilter_NamePattern</b> filters could exist.

### -field FsrmReportFilter_Property:8

The report will show only files that contain the specified property.

Applies to the <b>FsrmReportType_FilesByProperty</b> and 
       <b>FsrmReportType_FoldersByProperty</b> report types.

## -remarks

The value for the filter is specified when you call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreport-setfilter">IFsrmReport::SetFilter</a> or 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setdefaultfilter">IFsrmReportManager::SetDefaultFilter</a> 
    method to specify the filter. For example, you set the <i>filterValue</i> parameter to the 
    filter's value when calling <b>SetFilter</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreport-getfilter">IFsrmReport::GetFilter</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreport-setfilter">IFsrmReport::SetFilter</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-getdefaultfilter">IFsrmReportManager::GetDefaultFilter</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-isfiltervalidforreporttype">IFsrmReportManager::IsFilterValidForReportType</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setdefaultfilter">IFsrmReportManager::SetDefaultFilter</a>
