---
UID: NC:winwlx.PWLX_SET_RETURN_DESKTOP
title: PWLX_SET_RETURN_DESKTOP
author: windows-sdk-content
description: Called by GINA to specify the alternate application desktop that Winlogon will switch to when the current secure attention sequence (SAS) event processing function is complete.
old-location: security\wlxsetreturndesktop.htm
tech.root: secauthn
ms.assetid: 539e81d9-6362-4476-bdbc-849fb905b268
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: PWLX_SET_RETURN_DESKTOP, PWLX_SET_RETURN_DESKTOP callback, WlxSetReturnDesktop, WlxSetReturnDesktop callback function [Security], _gina_wlxsetreturndesktop, security.wlxsetreturndesktop, winwlx/WlxSetReturnDesktop
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
 - WlxSetReturnDesktop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_SET_RETURN_DESKTOP callback function


## -description


<p class="CCE_Message">[The WlxSetReturnDesktop function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to specify the alternate application desktop that <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> will switch to when the current <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">secure attention sequence</a> (SAS) event processing function is complete.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


### -param pDesktop [in]

Pointer to desktop information about the alternate desktop. This desktop is created by calling the 
<a href="https://msdn.microsoft.com/6985e858-f914-426a-91b4-cf8c3f604318">WlxCreateUserDesktop</a> function.


## -returns



The <b>WlxSetReturnDesktop</b> function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The function call was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The function call failed to set the return desktop.

</td>
</tr>
</table>
 




## -remarks



<b>WlxSetReturnDesktop</b> can be called only within 
<a href="https://msdn.microsoft.com/d60d1464-1948-444c-801a-dde17905091b">WlxLoggedOnSAS</a> or 
<a href="https://msdn.microsoft.com/7a9f8b00-857a-432e-bb49-2251504c46a0">WlxWkstaLockedSAS</a> routines. Attempts to call this function at other times will fail.

If a handle to the desktop is provided, Winlogon will duplicate the handle. If no handle is provided, Winlogon will attempt to open the desktop named in the <i>pDesktop</i> parameter. If the provided desktop is not valid or is the Winlogon or screen saver desktop, the call will fail.




## -see-also




<a href="https://msdn.microsoft.com/6985e858-f914-426a-91b4-cf8c3f604318">WlxCreateUserDesktop</a>



<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>



<a href="https://msdn.microsoft.com/d60d1464-1948-444c-801a-dde17905091b">WlxLoggedOnSAS</a>



<a href="https://msdn.microsoft.com/7a9f8b00-857a-432e-bb49-2251504c46a0">WlxWkstaLockedSAS</a>
 

 

