---
UID: NF:winwlx.WlxActivateUserShell
title: WlxActivateUserShell function (winwlx.h)
description: Activates the user shell program.
helpviewer_keywords: ["WlxActivateUserShell","WlxActivateUserShell function [Security]","_gina_wlxactivateusershell","security.wlxactivateusershell","winwlx/WlxActivateUserShell"]
old-location: security\wlxactivateusershell.htm
tech.root: security
ms.assetid: 0db6653b-ec6f-4b2b-9371-b73d73be1f7b
ms.date: 12/05/2018
ms.keywords: WlxActivateUserShell, WlxActivateUserShell function [Security], _gina_wlxactivateusershell, security.wlxactivateusershell, winwlx/WlxActivateUserShell
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WlxActivateUserShell
 - winwlx/WlxActivateUserShell
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxActivateUserShell
---

# WlxActivateUserShell function


## -description

<p class="CCE_Message">[The WlxActivateUserShell function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Activates the user shell program.

The <b>WlxActivateUserShell</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function following a successful logon to request that the GINA activate the shell program of the user.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. This is the context value that the GINA returns when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

### -param pszDesktopName [in]

A pointer to a null-terminated wide character string that specifies the name of the desktop where the shell will start. Pass this string to the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> or 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function through the <b>lpDesktop</b> member of the 
<a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure.

### -param pszMprLogonScript [in]

A pointer to a null-terminated wide character string that specifies any script names returned from the network provider DLLs. Network provider DLLs can return scripts to be executed during logon; however, the GINA may ignore them.

### -param pEnvironment [in]

Specifies the initial environment variables for the process. Winlogon creates a copy of the environment and hands it off to the GINA. The GINA can modify this environment before using it to initialize the user's shell. The GINA should call the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a> function to free the memory allocated for <i>pEnvironment</i>.

## -returns

If the function successfully starts a shell process, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. When <b>FALSE</b> is returned, Winlogon cancels the logon in process.

## -remarks

Before calling <b>WlxActivateUserShell</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

Always activate the user shell program in <b>WlxActivateUserShell</b> rather than 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxloggedoutsas">WlxLoggedOutSAS</a>. This gives Winlogon a chance to update its state, including setting workstation and desktop protections, before any logged-on user processes are allowed to run.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxloggedoutsas">WlxLoggedOutSAS</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxlogoff">WlxLogoff</a>