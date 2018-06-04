---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

