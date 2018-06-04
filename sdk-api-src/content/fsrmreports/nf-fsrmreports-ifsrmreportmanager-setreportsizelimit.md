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

# IFsrmReportManager::SetReportSizeLimit


## -description


Sets the current value of the specified report size limit.


## -parameters




### -param limit [in]

Identifies the limit which is used to limit the files listed in a report. For possible values, see the 
      <a href="https://msdn.microsoft.com/225c583c-679c-43b4-85f4-3f2294fa7bc3">FsrmReportLimit</a> enumeration.


### -param limitValue [in]

The limit. Must be greater than zero. You can specify the variant as a short, int, or long that is either 
      signed or unsigned. The method will also accept a string value. The method must be able to convert the value to 
      a positive, long number. For example, to pass the value as a long, set the variant type to 
      <b>VT_I4</b> and then set the <b>lVal</b> member of the variant to the 
      limit value.


## -returns



The method returns the following return values.




## -remarks



The following list lists the default limits for the 
     <a href="https://msdn.microsoft.com/225c583c-679c-43b4-85f4-3f2294fa7bc3">FsrmReportLimit</a> enumeration values used for 
     the <i>limit</i> parameter.

<table>
<tr>
<th>Limit</th>
<th>Default value</th>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxDuplicateGroups</b></td>
<td>100 duplicate groups</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFiles</b></td>
<td>1,000 files</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFileGroups</b></td>
<td>10 groups</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFileScreenEvents</b></td>
<td>1,000 file screen events</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFilesPerDuplGroup</b></td>
<td>10 files per duplicate group</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFilesPerFileGroup</b></td>
<td>100 files per group</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFilesPerOwner</b></td>
<td>100 files per owner</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFilesPerPropertyValue</b></td>
<td>100 files per property</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxOwners</b></td>
<td>10 owners</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxPropertyValues</b></td>
<td>10 properties</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxQuotas</b></td>
<td>1,000 quotas</td>
</tr>
<tr>
<td><b>FsrmReportLimit_MaxFolders</b></td>
<td>1,000 folders</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>



<a href="https://msdn.microsoft.com/112ed457-1083-4550-abd6-933f4b128e9a">IFsrmReportManager</a>
 

 

