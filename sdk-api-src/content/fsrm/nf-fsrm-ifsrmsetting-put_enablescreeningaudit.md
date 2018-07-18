---
UID: NF:fsrm.IFsrmSetting.put_EnableScreeningAudit
title: IFsrmSetting::put_EnableScreeningAudit
author: windows-sdk-content
description: Retrieves or sets a value that determines whether FSRM keeps audit records of the file screen violations.
old-location: fsrm\ifsrmsetting_enablescreeningaudit.htm
old-project: fsrm
ms.assetid: 6d185eca-6c14-4cd9-bb12-95499cde1050
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: EnableScreeningAudit property [File Server Resource Manager], EnableScreeningAudit property [File Server Resource Manager],FsrmSetting class, EnableScreeningAudit property [File Server Resource Manager],IFsrmSetting interface, FsrmSetting class [File Server Resource Manager],EnableScreeningAudit property, IFsrmSetting interface [File Server Resource Manager],EnableScreeningAudit property, IFsrmSetting.EnableScreeningAudit, IFsrmSetting.put_EnableScreeningAudit, IFsrmSetting::EnableScreeningAudit, IFsrmSetting::get_EnableScreeningAudit, IFsrmSetting::put_EnableScreeningAudit, fs.ifsrmsetting_enablescreeningaudit, fsrm.ifsrmsetting_enablescreeningaudit, fsrm/IFsrmSetting::EnableScreeningAudit, fsrm/IFsrmSetting::get_EnableScreeningAudit, fsrm/IFsrmSetting::put_EnableScreeningAudit, put_EnableScreeningAudit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, FsrmTlb.h
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
req.typenames: FILTERED_DATA_SOURCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmSetting.EnableScreeningAudit
 - IFsrmSetting.get_EnableScreeningAudit
 - IFsrmSetting.put_EnableScreeningAudit
 - FsrmSetting.EnableScreeningAudit
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmSetting::put_EnableScreeningAudit


## -description


Retrieves or sets a value that determines whether FSRM keeps audit records of the file screen 
    violations.

This property is read/write.


## -parameters


## -remarks



The records are included in a File Screen Audit report. An audit record contains the following items:

<ul>
<li>Folder path</li>
<li>Id</li>
<li>Blocked file group name</li>
<li>File screen mode</li>
<li>Time stamp of when the violation occurred</li>
<li>The name of the process image that generated the prohibited IO, if available</li>
<li>The SID of the user principal that issued the prohibited IO, if available</li>
<li>The full path of the prohibited file</li>
<li>The server name</li>
</ul>
If this property is false and a report specifies the 
    <b>FsrmReportType_FileScreenAudit</b> report type, the report will succeed but will not 
    contain any audit information (or will contain audits that were done before auditing was disabled).


#### Examples

For an example, see <a href="https://msdn.microsoft.com/432fbaaa-7ddb-4d8c-bfbe-40cd26b08f9b">IFsrmSetting</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c27393a-9a84-4147-a7e0-582c0bf2d918">FsrmSetting</a>



<a href="https://msdn.microsoft.com/432fbaaa-7ddb-4d8c-bfbe-40cd26b08f9b">IFsrmSetting</a>
 

 

