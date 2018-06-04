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
 

 

