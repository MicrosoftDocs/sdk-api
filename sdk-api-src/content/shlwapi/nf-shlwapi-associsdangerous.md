---
UID: NF:shlwapi.AssocIsDangerous
title: AssocIsDangerous function
author: windows-sdk-content
description: Determines whether a file type is considered a potential security risk.
old-location: shell\AssocIsDangerous.htm
tech.root: shell
ms.assetid: 4e0bc3ce-f9d2-4766-8b19-c0954d71e890
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AssocIsDangerous, AssocIsDangerous function [Windows Shell], _shell_AssocIsDangerous, shell.AssocIsDangerous, shlwapi/AssocIsDangerous
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
api_name:
 - AssocIsDangerous
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 6.01
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



Files that are determined to be potentially dangerous, such as .exe files, should be handled with more care than other files. For example, Windows Internet Explorer version 6.01 or later uses <b>AssocIsDangerous</b> to determine whether it should issue stronger warning language in its download dialog box. <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> uses <b>AssocIsDangerous</b> to trigger zone checking using the methods of the <a href="ie.IInternetSecurityManager_Interface">IInternetSecurityManager</a> interface in conjunction with the <a href="ie.URL_Action_Flags">URLACTION_SHELL_SHELLEXECUTE</a> flag.

The determination of a file's potential risk is made by checking its type against several sources, including a list of known dangerous types and the presence of the FTA_AlwaysUnsafe flag in the registry. On systems running Windows XPService Pack 1 (SP1) or later or Windows Server 2003, it also uses the <a href="https://msdn.microsoft.com/f122ceaa-65bb-4cfe-a760-adf4f910c487">SaferiIsExecutableFileType</a> function to determine whether a file type is executable.

Applications that can take advantage of <b>AssocIsDangerous</b> include email programs, browsers, chat clients capable of downloading files, and any application that moves files or data from one zone of trust to another.




## -see-also




<a href="https://msdn.microsoft.com/055648cd-46ce-4e61-80b2-bcf1d1823e20">File Types</a>



<a href="https://msdn.microsoft.com/f122ceaa-65bb-4cfe-a760-adf4f910c487">SaferiIsExecutableFileType</a>
 

 

