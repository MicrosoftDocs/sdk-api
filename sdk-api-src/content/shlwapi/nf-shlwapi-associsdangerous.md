---
UID: NF:shlwapi.AssocIsDangerous
title: AssocIsDangerous function (shlwapi.h)
description: Determines whether a file type is considered a potential security risk.
helpviewer_keywords: ["AssocIsDangerous","AssocIsDangerous function [Windows Shell]","_shell_AssocIsDangerous","shell.AssocIsDangerous","shlwapi/AssocIsDangerous"]
old-location: shell\AssocIsDangerous.htm
tech.root: shell
ms.assetid: 4e0bc3ce-f9d2-4766-8b19-c0954d71e890
ms.date: 12/05/2018
ms.keywords: AssocIsDangerous, AssocIsDangerous function [Windows Shell], _shell_AssocIsDangerous, shell.AssocIsDangerous, shlwapi/AssocIsDangerous
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 6.01 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 6.01
ms.custom: 19H1
f1_keywords:
 - AssocIsDangerous
 - shlwapi/AssocIsDangerous
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - ext-ms-win-shell-shlwapi-l1-1-2.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
api_name:
 - AssocIsDangerous
---

# AssocIsDangerous function


## -description

Determines whether a file type is considered a potential security risk.

## -parameters

### -param pszAssoc [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the type of file in question. This may be either an extension such as ".exe" or a progid such as "exefile".

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the file type is considered dangerous; otherwise, <b>FALSE</b>.

## -remarks

Files that are determined to be potentially dangerous, such as .exe files, should be handled with more care than other files. For example, Windows Internet Explorer version 6.01 or later uses <b>AssocIsDangerous</b> to determine whether it should issue stronger warning language in its download dialog box. <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> uses <b>AssocIsDangerous</b> to trigger zone checking using the methods of the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537130(v=vs.85)">IInternetSecurityManager</a> interface in conjunction with the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)">URLACTION_SHELL_SHELLEXECUTE</a> flag.

The determination of a file's potential risk is made by checking its type against several sources, including a list of known dangerous types and the presence of the FTA_AlwaysUnsafe flag in the registry. On systems running Windows XPService Pack 1 (SP1) or later or Windows Server 2003, it also uses the <a href="/windows/desktop/api/winsafer/nf-winsafer-saferiisexecutablefiletype">SaferiIsExecutableFileType</a> function to determine whether a file type is executable.

Applications that can take advantage of <b>AssocIsDangerous</b> include email programs, browsers, chat clients capable of downloading files, and any application that moves files or data from one zone of trust to another.

## -see-also

<a href="/windows/desktop/shell/fa-file-types">File Types</a>



<a href="/windows/desktop/api/winsafer/nf-winsafer-saferiisexecutablefiletype">SaferiIsExecutableFileType</a>