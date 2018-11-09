---
UID: NC:winwlx.PWLX_CLOSE_USER_DESKTOP
title: PWLX_CLOSE_USER_DESKTOP
author: windows-sdk-content
description: Called by GINA to close an alternate user desktop and clean up after the desktop is closed.
old-location: security\wlxcloseuserdesktop.htm
tech.root: secauthn
ms.assetid: ad910f0b-f8fb-4246-830e-1edb23e06f36
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: PWLX_CLOSE_USER_DESKTOP, PWLX_CLOSE_USER_DESKTOP callback, WlxCloseUserDesktop, WlxCloseUserDesktop callback function [Security], _gina_wlxcloseuserdesktop, security.wlxcloseuserdesktop, winwlx/WlxCloseUserDesktop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
 - WlxCloseUserDesktop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_CLOSE_USER_DESKTOP callback function


## -description


<p class="CCE_Message">[The WlxCloseUserDesktop function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to close an alternate user desktop and clean up after the desktop is closed.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


### -param pDesktop [in]

Specifies a pointer to a 
<a href="https://msdn.microsoft.com/3cde1b9e-5109-400d-a67f-1e263f2283d1">WLX_DESKTOP</a> structure, obtained by calling the 
<a href="https://msdn.microsoft.com/6985e858-f914-426a-91b4-cf8c3f604318">WlxCreateUserDesktop</a> function.


### -param hToken [in]

Specifies the handle to the token of the user whose desktop is to be closed.


## -returns



If the function successfully closes the desktop, the return value is <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.




## -remarks



In addition to closing the desktop, this function will modify access to the parent window station to remove <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ACEs</a> added during the creation of the user desktop.




## -see-also




<a href="https://msdn.microsoft.com/3cde1b9e-5109-400d-a67f-1e263f2283d1">WLX_DESKTOP</a>



<a href="https://msdn.microsoft.com/6985e858-f914-426a-91b4-cf8c3f604318">WlxCreateUserDesktop</a>



<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

