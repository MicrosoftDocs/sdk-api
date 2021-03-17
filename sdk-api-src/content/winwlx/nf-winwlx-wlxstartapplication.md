---
UID: NF:winwlx.WlxStartApplication
title: WlxStartApplication function (winwlx.h)
description: Winlogon calls this function when the system needs an application to be started in the context of the user.
helpviewer_keywords: ["WlxStartApplication","WlxStartApplication function [Security]","_gina_wlxstartapplication","security.wlxstartapplication","winwlx/WlxStartApplication"]
old-location: security\wlxstartapplication.htm
tech.root: security
ms.assetid: ad6b520a-56b7-4d22-b4d4-4b45e9e42a9f
ms.date: 12/05/2018
ms.keywords: WlxStartApplication, WlxStartApplication function [Security], _gina_wlxstartapplication, security.wlxstartapplication, winwlx/WlxStartApplication
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
 - WlxStartApplication
 - winwlx/WlxStartApplication
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
 - WlxStartApplication
---

# WlxStartApplication function


## -description

<p class="CCE_Message">[The WlxStartApplication function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxStartApplication</b> function can be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function when the system needs an application to be started in the <a href="/windows/desktop/SecGloss/c-gly">context</a> of the user.

There are two reasons that the  system might need an application to start in the context of the user:
<ul>
<li>Windows Explorer has quit unexpectedly and needs to be restarted.</li>
<li>The extended task manager needs to run.</li>
</ul><div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>The GINA can override this behavior, if appropriate, by using the <b>WlxStartApplication</b> function.

## -parameters

### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

### -param pszDesktopName [in]

Specifies the name of the desktop on which to start the application. Pass this string to the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> or 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function through the <b>lpDesktop</b> member of the 
<a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure.

### -param pEnvironment [in]

Specifies the initial environment for the process. Winlogon creates this environment and hands it off to the GINA. The GINA can modify this environment before using it to initialize the shell of the user. When the GINA has finished using this environment, it must free the memory allocated for <i>pEnvironment</i> by calling the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a> function.

### -param pszCmdLine [in]

The program to execute.

## -returns

If the function successfully starts the application, the function returns <b>TRUE</b>.

If the function fails or the application did not start, the function returns <b>FALSE</b>.

## -remarks

Before calling <b>WlxStartApplication</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

If the <b>WlxStartApplication</b> function is not exported by the GINA, Winlogon will execute the process.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>