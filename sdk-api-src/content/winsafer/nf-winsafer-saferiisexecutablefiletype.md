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

# SaferiIsExecutableFileType function


## -description


The <b>SaferiIsExecutableFileType</b> function determines whether a specified file is an executable file. Applications use this function to determine whether a file is an executable file, and if it is, then the application can take security precautions to prevent invoking untrustworthy code.


## -parameters




### -param szFullPathname

TBD


### -param bFromShellExecute [in]

Boolean value that determines whether .exe files are treated as executable files for the file type evaluation. Set this value to <b>TRUE</b> to omit .exe files from the evaluation or to <b>FALSE</b> to include them.


#### - szFullPath [in]

Pointer to a <b>null</b>-terminated <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> character string for the name of the file. The path is optional because only the file name extension is evaluated. The evaluation of the file name extension is not case-sensitive. This parameter cannot be <b>NULL</b> or an empty string, and the specified file must include a file name extension.


## -returns



If the function  successfully recognizes the file name's extension as an executable file type, the return value is <b>TRUE</b>.

If the function fails, or if <i>szFullPath</i> identifies a file name with a nonexecutable extension, the function returns <b>FALSE</b>.




## -remarks



The following file name extensions are examples of executable file types.  This is not a complete list.

<ul>
<li>.bat</li>
<li>.cmd</li>
<li>.com</li>
<li>.exe</li>
<li>.js</li>
<li>.lnk</li>
<li>.pif</li>
<li>.pl</li>
<li>.shs</li>
<li>.url</li>
<li>.vbs</li>
</ul>
The security policy Microsoft Management Console (MMC) snap-in (Secpol.msc) controls which extensions are considered executable file types.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To view or modify the extensions that are considered executable file types</b>

<ol>
<li>Run Secpol.msc.</li>
<li>Expand  <b>Software Restriction Policies</b>, and then double-click <b>Designated File Types</b>.</li>
</ol>
<div class="alert"><b>Note</b>  To view the <b>Designated File Types</b> property page, you may need to create  the <b>Software Restriction Policies</b> node. To create  the <b>Software Restriction Policies</b> node, follow the instructions that appear when you expand <b>Software Restriction Policies</b>.</div>
<div> </div>


