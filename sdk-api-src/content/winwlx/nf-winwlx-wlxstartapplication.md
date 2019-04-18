---
UID: NF:winwlx.WlxStartApplication
title: WlxStartApplication function (winwlx.h)
author: windows-sdk-content
description: Winlogon calls this function when the system needs an application to be started in the context of the user.
old-location: security\wlxstartapplication.htm
tech.root: SecAuthN
ms.assetid: ad6b520a-56b7-4d22-b4d4-4b45e9e42a9f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WlxStartApplication, WlxStartApplication function [Security], _gina_wlxstartapplication, security.wlxstartapplication, winwlx/WlxStartApplication
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
 - WlxStartApplication
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WlxStartApplication function


## -description


<p class="CCE_Message">[The WlxStartApplication function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxStartApplication</b> function can be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> calls this function when the system needs an application to be started in the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> of the user.

There are two reasons that the  system might need an application to start in the context of the user:
<ul>
<li>Windows Explorer has quit unexpectedly and needs to be restarted.</li>
<li>The extended task manager needs to run.</li>
</ul><div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>The GINA can override this behavior, if appropriate, by using the <b>WlxStartApplication</b> function.


## -parameters




### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


### -param pszDesktopName [in]

Specifies the name of the desktop on which to start the application. Pass this string to the 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> or 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function through the <b>lpDesktop</b> member of the 
<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure.


### -param pEnvironment [in]

Specifies the initial environment for the process. Winlogon creates this environment and hands it off to the GINA. The GINA can modify this environment before using it to initialize the shell of the user. When the GINA has finished using this environment, it must free the memory allocated for <i>pEnvironment</i> by calling the <a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a> function.


### -param pszCmdLine [in]

The program to execute.


## -returns



If the function successfully starts the application, the function returns <b>TRUE</b>.

If the function fails or the application did not start, the function returns <b>FALSE</b>.




## -remarks



Before calling <b>WlxStartApplication</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

If the <b>WlxStartApplication</b> function is not exported by the GINA, Winlogon will execute the process.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

