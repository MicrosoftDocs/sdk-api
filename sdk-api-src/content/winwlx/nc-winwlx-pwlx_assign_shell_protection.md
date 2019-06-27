---
UID: NC:winwlx.PWLX_ASSIGN_SHELL_PROTECTION
title: PWLX_ASSIGN_SHELL_PROTECTION (winwlx.h)
author: windows-sdk-content
description: Called by GINA to assign protection to the shell program of a newly logged-on user.
old-location: security\wlxassignshellprotection.htm
tech.root: SecAuthN
ms.assetid: 7a744bde-3354-4e55-a6be-08acb4085e8a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PWLX_ASSIGN_SHELL_PROTECTION, PWLX_ASSIGN_SHELL_PROTECTION callback, WlxAssignShellProtection, WlxAssignShellProtection callback function [Security], _gina_wlxassignshellprotection, security.wlxassignshellprotection, winwlx/WlxAssignShellProtection
ms.topic: callback
f1_keywords: 
 - "winwlx/WlxAssignShellProtection"
req.header: winwlx.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winwlx.h
api_name:
 - WlxAssignShellProtection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PWLX_ASSIGN_SHELL_PROTECTION callback function


## -description


<p class="CCE_Message">[The WlxAssignShellProtection function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://docs.microsoft.com/windows/desktop/SecGloss/g-gly">GINA</a> to assign protection to the shell program of a newly logged-on user.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>The shell process should be created in a suspended state, then the <b>WlxAssignShellProtection</b> function should be called to apply the correct protection to the shell process.

This function has been superseded by the Windows API 
<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function.


## -parameters




### -param hWlx [in]

Specifies the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/w-gly">Winlogon</a> handle passed to GINA in the 
<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.


### -param hToken [in]

Specifies the handle to a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">primary token</a>.


### -param hProcess [in]

Specifies the handle to the process to modify. The process must be created in the suspended state, and this should be the handle returned in the 
<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-_process_information">PROCESS_INFORMATION</a> structure.


### -param hThread [in]

Specifies the handle to the initial thread of the process.


## -returns



The <b>WlxAssignShellProtection</b> function returns any errors encountered while trying to assign protection.




## -remarks



The Windows API 
<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function supersedes <b>WlxAssignShellProtection</b>. Call <b>CreateProcessAsUser</b> in 
<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nf-winwlx-wlxactivateusershell">WlxActivateUserShell</a> to create the shell process and set its protections in a single call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nf-winwlx-wlxactivateusershell">WlxActivateUserShell</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>
 

 

