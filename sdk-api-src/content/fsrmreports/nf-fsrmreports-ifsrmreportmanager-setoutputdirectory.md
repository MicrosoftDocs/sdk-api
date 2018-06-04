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

# IFsrmReportManager::SetOutputDirectory


## -description


Sets the local directory path where reports are stored.


## -parameters




### -param context [in]

The report context (for example, if the report is scheduled or runs on demand). For possible values, see 
      the <a href="https://msdn.microsoft.com/02e18cc2-7c5e-473f-8a7f-e310bfb1c57d">FsrmReportGenerationContext</a> 
      enumeration.


### -param path [in]

The full path to the local directory where the reports are stored. The path can contain environment 
      variables. The path is limited to 150 characters.


## -returns



The method returns the following return values.




## -remarks



The reports are stored in the following folders under the given path.

<table>
<tr>
<th>Context</th>
<th>Folder</th>
</tr>
<tr>
<td><b>FsrmReportGenerationContext_ScheduledReport</b></td>
<td>Scheduled</td>
</tr>
<tr>
<td><b>FsrmReportGenerationContext_InteractiveReport</b></td>
<td>Interactive</td>
</tr>
<tr>
<td><b>FsrmReportGenerationContext_IncidentReport</b></td>
<td>Incident</td>
</tr>
</table>
 

For example, if <i>path</i> is set to "C:\StorageReports" and 
    <i>context</i> is set to 
    <b>FsrmReportGenerationContext_ScheduledReport</b>, the path for the scheduled reports would 
    be "C:\StorageReports\Scheduled".

The default output directories are:

<ul>
<li>"%systemdrive%\StorageReports\Scheduled"</li>
<li>"%systemdrive%\StorageReports\Incident"</li>
<li>"%systemdrive%\StorageReports\Interactive"</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>



<a href="https://msdn.microsoft.com/112ed457-1083-4550-abd6-933f4b128e9a">IFsrmReportManager</a>
 

 

