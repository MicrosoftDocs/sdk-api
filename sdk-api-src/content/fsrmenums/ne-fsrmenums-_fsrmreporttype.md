---
UID: NE:fsrmenums._FsrmReportType
title: "_FsrmReportType"
author: windows-sdk-content
description: Defines the types of reports that you can generate.
old-location: fsrm\fsrmreporttype.htm
old-project: fsrm
ms.assetid: 6fb5cb02-371b-4d07-9f13-d0409d5835d4
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: FsrmReportType, FsrmReportType enumeration [File Server Resource Manager], FsrmReportType_AutomaticClassification, FsrmReportType_DuplicateFiles, FsrmReportType_Expiration, FsrmReportType_ExportReport, FsrmReportType_FileScreenAudit, FsrmReportType_FilesByOwner, FsrmReportType_FilesByProperty, FsrmReportType_FilesByType, FsrmReportType_FoldersByProperty, FsrmReportType_LargeFiles, FsrmReportType_LeastRecentlyAccessed, FsrmReportType_MostRecentlyAccessed, FsrmReportType_QuotaUsage, FsrmReportType_Unknown, _FsrmReportType, fs.fsrmreporttype, fsrm.fsrmreporttype, fsrmenums/FsrmReportType, fsrmenums/FsrmReportType_AutomaticClassification, fsrmenums/FsrmReportType_DuplicateFiles, fsrmenums/FsrmReportType_Expiration, fsrmenums/FsrmReportType_ExportReport, fsrmenums/FsrmReportType_FileScreenAudit, fsrmenums/FsrmReportType_FilesByOwner, fsrmenums/FsrmReportType_FilesByProperty, fsrmenums/FsrmReportType_FilesByType, fsrmenums/FsrmReportType_FoldersByProperty, fsrmenums/FsrmReportType_LargeFiles, fsrmenums/FsrmReportType_LeastRecentlyAccessed, fsrmenums/FsrmReportType_MostRecentlyAccessed, fsrmenums/FsrmReportType_QuotaUsage, fsrmenums/FsrmReportType_Unknown
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
req.typenames: FsrmReportType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmReportType
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# _FsrmReportType enumeration


## -description


Defines the types of reports that you can generate.


## -enum-fields




### -field FsrmReportType_Unknown

The report type is unknown. Do not use this flag.


### -field FsrmReportType_LargeFiles

Lists files that are larger than a specified size. Set the filter value to the size, in bytes.


### -field FsrmReportType_FilesByType

Lists groups of files. Create a file group and use file name patterns to specify the members of the group. 
      Set the filter value to the name of the file group.


### -field FsrmReportType_LeastRecentlyAccessed

Lists files that have not been accessed in the last <i>n</i> days. Specify the filter 
      value in days.


### -field FsrmReportType_MostRecentlyAccessed

Lists files that have been accessed in the last <i>n</i> days. Specify the filter value 
      in days.


### -field FsrmReportType_QuotaUsage

Lists quotas that exceed the specified threshold. Set the filter value to the threshold.


### -field FsrmReportType_FilesByOwner

Lists files grouped by their owner. Set the filter value to the list of owners whose files you want 
      included in the report.


### -field FsrmReportType_ExportReport

Lists all files in the scope of the report job; there is no filtering. You can specify the XML or CSV file 
       formats only for this report type. This report cannot be sent through email.

For an action report, the scope is based on the quota or file screen event that initiated the report.


### -field FsrmReportType_DuplicateFiles

Lists duplicate files. All files with the same file name, file size, and last modify time under the scope 
      of the report job are considered duplicates. For example, if the scope of the report is C:\ and 
      D:\ and file file1.txt exists in C:\<i>folder1</i>\, 
      C:\<i>folder2</i>\ and D:\<i>folder1</i>\ with 
      the same modify time and file size, then the files are considered duplicates.


### -field FsrmReportType_FileScreenAudit

Lists file screening events that have occurred.


### -field FsrmReportType_FilesByProperty

Lists files, grouped by property value, that contain the specified property (you can specify only one 
       property on which to report).

<b>Windows Server 2008:  </b>This report type is not supported before Windows Server 2008 R2.


### -field FsrmReportType_AutomaticClassification

For internal use only; do not specify.

<b>Windows Server 2008:  </b>This report type is not supported before Windows Server 2008 R2.


### -field FsrmReportType_Expiration

For internal use only; do not specify.

<b>Windows Server 2008:  </b>This report type is not supported before Windows Server 2008 R2.


### -field FsrmReportType_FoldersByProperty

Lists folders, grouped by property value, that contain the specified property (you can specify only one 
       property on which to report).

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This report type is not supported before Windows Server 2012.


## -remarks



To specify the values for report types that require a filter (for example, listing files over a specified 
    size), call the 
    <a href="https://msdn.microsoft.com/5a3165a9-8161-4dad-b8b9-d0c3f54f1803">IFsrmReportManager::SetDefaultFilter</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>



<a href="https://msdn.microsoft.com/942b9a7f-06b2-45bf-8398-b4c68a168a73">IFsrmActionReport::ReportTypes</a>



<a href="https://msdn.microsoft.com/0f23c03a-5f9b-4a0e-b9cc-399ca931b6f7">IFsrmReport::Type</a>



<a href="https://msdn.microsoft.com/484941d1-726c-4765-8652-bcb378f277b4">IFsrmReportJob::CreateReportCreateReport</a>



<a href="https://msdn.microsoft.com/5f3a587e-c3a8-47ee-80ac-afa0824a4585">IFsrmReportManager::GetDefaultFilter</a>



<a href="https://msdn.microsoft.com/e9f93b97-c8ac-441a-9f6b-87d45bd10cdf">IFsrmReportManager::IsFilterValidForReportType</a>



<a href="https://msdn.microsoft.com/5a3165a9-8161-4dad-b8b9-d0c3f54f1803">IFsrmReportManager::SetDefaultFilter</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>
 

 

