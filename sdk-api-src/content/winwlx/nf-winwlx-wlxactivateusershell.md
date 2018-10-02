---
UID: NF:winwlx.WlxActivateUserShell
title: WlxActivateUserShell function
author: windows-sdk-content
description: Activates the user shell program.
old-location: security\wlxactivateusershell.htm
tech.root: secauthn
ms.assetid: 0db6653b-ec6f-4b2b-9371-b73d73be1f7b
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: WlxActivateUserShell, WlxActivateUserShell function [Security], _gina_wlxactivateusershell, security.wlxactivateusershell, winwlx/WlxActivateUserShell
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - Winwlx.h
api_name:
 - WlxActivateUserShell
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WlxActivateUserShell function


## -description


<p class="CCE_Message">[The WlxActivateUserShell function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Activates the user shell program.

The <b>WlxActivateUserShell</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> calls this function following a successful logon to request that the GINA activate the shell program of the user.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. This is the context value that the GINA returns when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


### -param pszDesktopName [in]

A pointer to a null-terminated wide character string that specifies the name of the desktop where the shell will start. Pass this string to the 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> or 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function through the <b>lpDesktop</b> member of the 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure.


### -param pszMprLogonScript [in]

A pointer to a null-terminated wide character string that specifies any script names returned from the network provider DLLs. Network provider DLLs can return scripts to be executed during logon; however, the GINA may ignore them.


### -param pEnvironment [in]

Specifies the initial environment variables for the process. Winlogon creates a copy of the environment and hands it off to the GINA. The GINA can modify this environment before using it to initialize the user's shell. The GINA should call the <a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a> function to free the memory allocated for <i>pEnvironment</i>.


## -returns



If the function successfully starts a shell process, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. When <b>FALSE</b> is returned, Winlogon cancels the logon in process.




## -remarks



Before calling <b>WlxActivateUserShell</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

Always activate the user shell program in <b>WlxActivateUserShell</b> rather than 
<a href="https://msdn.microsoft.com/7f3996b6-7c99-42c5-a39f-8c67ff19a580">WlxLoggedOutSAS</a>. This gives Winlogon a chance to update its state, including setting workstation and desktop protections, before any logged-on user processes are allowed to run.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>



<a href="https://msdn.microsoft.com/7f3996b6-7c99-42c5-a39f-8c67ff19a580">WlxLoggedOutSAS</a>



<a href="https://msdn.microsoft.com/bbeafd41-fe01-497d-8514-a6c088a11d73">WlxLogoff</a>
 

 

