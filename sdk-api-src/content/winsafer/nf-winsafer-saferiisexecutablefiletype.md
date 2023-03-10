---
UID: NF:winsafer.SaferiIsExecutableFileType
title: SaferiIsExecutableFileType function (winsafer.h)
description: Determines whether a specified file is an executable file.
helpviewer_keywords: ["SaferiIsExecutableFileType","SaferiIsExecutableFileType function [Security]","security.saferiisexecutablefiletype","winsafer/SaferiIsExecutableFileType"]
old-location: security\saferiisexecutablefiletype.htm
tech.root: security
ms.assetid: f122ceaa-65bb-4cfe-a760-adf4f910c487
ms.date: 12/05/2018
ms.keywords: SaferiIsExecutableFileType, SaferiIsExecutableFileType function [Security], security.saferiisexecutablefiletype, winsafer/SaferiIsExecutableFileType
req.header: winsafer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SaferiIsExecutableFileType
 - winsafer/SaferiIsExecutableFileType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
api_name:
 - SaferiIsExecutableFileType
req.apiset: ext-ms-win-advapi32-safer-l1-1-0 (introduced in Windows 8)
---

# SaferiIsExecutableFileType function


## -description

The <b>SaferiIsExecutableFileType</b> function determines whether a specified file is an executable file. Applications use this function to determine whether a file is an executable file, and if it is, then the application can take security precautions to prevent invoking untrustworthy code.

## -parameters

### -param szFullPathname [in]

Pointer to a <b>null</b>-terminated <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> character string for the name of the file. The path is optional because only the file name extension is evaluated. The evaluation of the file name extension is not case-sensitive. This parameter cannot be <b>NULL</b> or an empty string, and the specified file must include a file name extension.

### -param bFromShellExecute [in]

Boolean value that determines whether .exe files are treated as executable files for the file type evaluation. Set this value to <b>TRUE</b> to omit .exe files from the evaluation or to <b>FALSE</b> to include them.

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

<p class="proch"><b>To view or modify the extensions that are considered executable file types</b>

<ol>
<li>Run Secpol.msc.</li>
<li>Expand  <b>Software Restriction Policies</b>, and then double-click <b>Designated File Types</b>.</li>
</ol>
<div class="alert"><b>Note</b>  To view the <b>Designated File Types</b> property page, you may need to create  the <b>Software Restriction Policies</b> node. To create  the <b>Software Restriction Policies</b> node, follow the instructions that appear when you expand <b>Software Restriction Policies</b>.</div>
<div> </div>
