---
UID: NE:fsrmenums._FsrmReportFilter
title: "_FsrmReportFilter"
author: windows-sdk-content
description: Defines the filters that you can use to limit the files that are included in a report.
old-location: fsrm\fsrmreportfilter.htm
old-project: fsrm
ms.assetid: 6f38ec9a-8876-44ce-9d44-f3982f1880ca
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: FsrmReportFilter, FsrmReportFilter enumeration [File Server Resource Manager], FsrmReportFilter_FileGroups, FsrmReportFilter_MaxAgeDays, FsrmReportFilter_MinAgeDays, FsrmReportFilter_MinQuotaUsage, FsrmReportFilter_MinSize, FsrmReportFilter_NamePattern, FsrmReportFilter_Owners, FsrmReportFilter_Property, _FsrmReportFilter, fs.fsrmreportfilter, fsrm.fsrmreportfilter, fsrmenums/FsrmReportFilter, fsrmenums/FsrmReportFilter_FileGroups, fsrmenums/FsrmReportFilter_MaxAgeDays, fsrmenums/FsrmReportFilter_MinAgeDays, fsrmenums/FsrmReportFilter_MinQuotaUsage, fsrmenums/FsrmReportFilter_MinSize, fsrmenums/FsrmReportFilter_NamePattern, fsrmenums/FsrmReportFilter_Owners, fsrmenums/FsrmReportFilter_Property
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
req.typenames: FsrmReportFilter
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmReportFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# _FsrmReportFilter enumeration


## -description


Defines the filters that you can use to limit the files that are included in a report.


## -enum-fields




### -field FsrmReportFilter_MinSize

The report will show only files that meet a minimum size.

Applies to the <b>FsrmReportType_LargeFiles</b> report type.


### -field FsrmReportFilter_MinAgeDays

The report will show only files that were accessed more than a minimum number of days ago.

Applies to the <b>FsrmReportType_LeastRecentlyAccessed</b> and 
       <b>FsrmReportType_FileScreenAudit</b> report types.


### -field FsrmReportFilter_MaxAgeDays

The report will show only files that were accessed prior to a maximum number of days ago.

Applies to the <b>FsrmReportType_MostRecentlyAccessed</b> report type.


### -field FsrmReportFilter_MinQuotaUsage

The report will show only quotas that meet a certain disk space usage level.

Applies to the <b>FsrmReportType_QuotaUsage</b> report type.


### -field FsrmReportFilter_FileGroups

The report will show only files from a specified set of file groups.

Applies to the <b>FsrmReportType_FilesByType</b> report type.


### -field FsrmReportFilter_Owners

The report will show only files that belong to specified owners. The format of the owner string can be either 
       the user principal name 
       ("<i>UserName</i>@<i>Domain</i>" or 
       "<i>Domain</i>\<i>UserName</i>") or a SID in string 
       format.

Applies to the <b>FsrmReportType_FilesByOwner</b> report type.


### -field FsrmReportFilter_NamePattern

The report will show only files with names that match the specified pattern.

Applies to the <b>FsrmReportType_LargeFiles</b>, 
       <b>FsrmReportType_MostRecentlyAccessed</b>, 
       <b>FsrmReportType_LeastRecentlyAccessed</b>, 
       <b>FsrmReportType_FilesByOwner</b>, and  
       <b>FsrmReportType_FilesByProperty</b> report types. For these report types, multiple 
       filters could exist. For example, for the <b>FsrmReportType_LargeFiles</b> report type, 
       both the <b>FsrmReportFilter_MinSize</b> and 
       <b>FsrmReportFilter_NamePattern</b> filters could exist.


### -field FsrmReportFilter_Property

The report will show only files that contain the specified property.

Applies to the <b>FsrmReportType_FilesByProperty</b> and 
       <b>FsrmReportType_FoldersByProperty</b> report types.


## -remarks



The value for the filter is specified when you call the 
    <a href="https://msdn.microsoft.com/6d36e3e2-7826-4bae-943c-3ab73404534c">IFsrmReport::SetFilter</a> or 
    <a href="https://msdn.microsoft.com/5a3165a9-8161-4dad-b8b9-d0c3f54f1803">IFsrmReportManager::SetDefaultFilter</a> 
    method to specify the filter. For example, you set the <i>filterValue</i> parameter to the 
    filter's value when calling <b>SetFilter</b>.




## -see-also




<a href="https://msdn.microsoft.com/991b0009-7ed9-4d75-af03-1b76aa8be70c">IFsrmReport::GetFilter</a>



<a href="https://msdn.microsoft.com/6d36e3e2-7826-4bae-943c-3ab73404534c">IFsrmReport::SetFilter</a>



<a href="https://msdn.microsoft.com/5f3a587e-c3a8-47ee-80ac-afa0824a4585">IFsrmReportManager::GetDefaultFilter</a>



<a href="https://msdn.microsoft.com/e9f93b97-c8ac-441a-9f6b-87d45bd10cdf">IFsrmReportManager::IsFilterValidForReportType</a>



<a href="https://msdn.microsoft.com/5a3165a9-8161-4dad-b8b9-d0c3f54f1803">IFsrmReportManager::SetDefaultFilter</a>
 

 

