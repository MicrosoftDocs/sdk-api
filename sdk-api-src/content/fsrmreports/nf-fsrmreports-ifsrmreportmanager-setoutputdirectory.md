---
UID: NF:fsrmreports.IFsrmReportManager.SetOutputDirectory
title: IFsrmReportManager::SetOutputDirectory (fsrmreports.h)
description: Sets the local directory path where reports are stored.
helpviewer_keywords: ["FsrmReportManager class [File Server Resource Manager]","SetOutputDirectory method","IFsrmReportManager interface [File Server Resource Manager]","SetOutputDirectory method","IFsrmReportManager.SetOutputDirectory","IFsrmReportManager::SetOutputDirectory","SetOutputDirectory","SetOutputDirectory method [File Server Resource Manager]","SetOutputDirectory method [File Server Resource Manager]","FsrmReportManager class","SetOutputDirectory method [File Server Resource Manager]","IFsrmReportManager interface","fs.ifsrmreportmanager_setoutputdirectory","fsrm.ifsrmreportmanager_setoutputdirectory","fsrmreports/IFsrmReportManager::SetOutputDirectory"]
old-location: fsrm\ifsrmreportmanager_setoutputdirectory.htm
tech.root: fsrm
ms.assetid: 5bbc4255-1fed-45c5-bb13-41ee7c47ed56
ms.date: 12/05/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager],SetOutputDirectory method, IFsrmReportManager interface [File Server Resource Manager],SetOutputDirectory method, IFsrmReportManager.SetOutputDirectory, IFsrmReportManager::SetOutputDirectory, SetOutputDirectory, SetOutputDirectory method [File Server Resource Manager], SetOutputDirectory method [File Server Resource Manager],FsrmReportManager class, SetOutputDirectory method [File Server Resource Manager],IFsrmReportManager interface, fs.ifsrmreportmanager_setoutputdirectory, fsrm.ifsrmreportmanager_setoutputdirectory, fsrmreports/IFsrmReportManager::SetOutputDirectory
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
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmReportManager::SetOutputDirectory
 - fsrmreports/IFsrmReportManager::SetOutputDirectory
dev_langs:
 - c++
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
---

# IFsrmReportManager::SetOutputDirectory


## -description

Sets the local directory path where reports are stored.

## -parameters

### -param context [in]

The report context (for example, if the report is scheduled or runs on demand). For possible values, see 
      the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportgenerationcontext">FsrmReportGenerationContext</a> 
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

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportmanager">IFsrmReportManager</a>