---
UID: NF:fsrmreports.IFsrmReportManager.SetOutputDirectory
title: IFsrmReportManager::SetOutputDirectory
author: windows-sdk-content
description: Sets the local directory path where reports are stored.
old-location: fsrm\ifsrmreportmanager_setoutputdirectory.htm
old-project: fsrm
ms.assetid: 5bbc4255-1fed-45c5-bb13-41ee7c47ed56
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager],SetOutputDirectory method, IFsrmReportManager interface [File Server Resource Manager],SetOutputDirectory method, IFsrmReportManager.SetOutputDirectory, IFsrmReportManager::SetOutputDirectory, SetOutputDirectory, SetOutputDirectory method [File Server Resource Manager], SetOutputDirectory method [File Server Resource Manager],FsrmReportManager class, SetOutputDirectory method [File Server Resource Manager],IFsrmReportManager interface, fs.ifsrmreportmanager_setoutputdirectory, fsrm.ifsrmreportmanager_setoutputdirectory, fsrmreports/IFsrmReportManager::SetOutputDirectory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmreports.h
req.include-header: FsrmReports.h, FsrmTlb.h
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmReportManager.SetOutputDirectory
 - FsrmReportManager.SetOutputDirectory
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
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
 

 

