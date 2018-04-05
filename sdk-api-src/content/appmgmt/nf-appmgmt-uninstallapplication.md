---
UID: NF:appmgmt.UninstallApplication
title: UninstallApplication function
author: windows-driver-content
description: The UninstallApplication function uninstalls a group policy application that handles setup and installation using Windows Installer .msi files.
old-location: policy\uninstallapplication.htm
old-project: Policy
ms.assetid: d45494e2-d86e-4d94-a158-4024eacf46a2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: UninstallApplication, UninstallApplication function [Group Policy], appmgmt/UninstallApplication, policy.uninstallapplication
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: appmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.typenames: INSTALLSPECTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
api_name:
-	UninstallApplication
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# UninstallApplication function


## -description


The
    <b>UninstallApplication</b> function uninstalls a group policy  application that handles setup and installation using <a href="setup.windows_installer_start_page">Windows Installer</a> .msi files. The <b>UninstallApplication</b> function should only be called in the context of the user for whom the user group policy application has previously attempted an uninstall by calling the <a href="https://msdn.microsoft.com/06f341ac-badd-47a0-af86-4fb76bf528d6">MsiConfigureProduct</a> function. The <a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a> function can install group policy applications.
<div class="alert"><b>Note</b>  Failure to call <b>UninstallApplication</b> as part of the protocol for uninstalling a group policy-based application can cause the <a href="https://msdn.microsoft.com/c3367738-21c9-4159-bc33-2529a60f0e39">Resultant Set of Policy (RSoP)</a> to indicate inaccurate information.</div><div> </div>

## -parameters




### -param ProductCode [in]

The <a href="setup.windows_installer_start_page">Windows Installer</a> product code of the product being uninstalled. The <a href="https://msdn.microsoft.com/6fbad59b-27b7-4ac1-bad5-8a608c7b270f">product code</a> of the application should be provided in the form of  a <a href="https://msdn.microsoft.com/9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8">Windows Installer GUID</a> as a string with braces.


### -param dwStatus [in]

The status of the uninstall attempt. The <i>dwStatus</i> parameter is the Windows success code of the uninstall attempt returned by <a href="https://msdn.microsoft.com/06f341ac-badd-47a0-af86-4fb76bf528d6">MsiConfigureProduct</a>.  The system can use this to ensure that the  <a href="https://msdn.microsoft.com/c3367738-21c9-4159-bc33-2529a60f0e39">Resultant Set of Policy (RSoP)</a> indicates whether the uninstall failed or succeeded.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a> or the header file WinError.h.




## -remarks



Remove a group policy application that uses .msi files by calling  the <a href="setup.windows_installer_start_page">Windows Installer</a> function <a href="https://msdn.microsoft.com/06f341ac-badd-47a0-af86-4fb76bf528d6">MsiConfigureProduct</a> to uninstall the application. Then call <b>UninstallApplication</b>  to  inform the system that the application is no longer managed on the client by Group Policy.  <b>UninstallApplication</b> should be called even if the uninstall fails because this enables the system to keep the <a href="https://msdn.microsoft.com/c3367738-21c9-4159-bc33-2529a60f0e39">Resultant Set of Policy (RSoP)</a> accurate.

Remove applications installed using software installation settings (.zap files) by calling  the uninstall function or command  specific for the installation application. For information about using installation applications other than  the <a href="setup.windows_installer_start_page">Windows Installer</a> see article 231747, "<a href="Http://go.microsoft.com/fwlink/p/?linkid=83984">How to Publish non-MSI Programs with .zap Files</a>," in the Microsoft Knowledge Base.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a>



<a href="https://msdn.microsoft.com/06f341ac-badd-47a0-af86-4fb76bf528d6">MsiConfigureProduct</a>
 

 

