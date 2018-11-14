---
UID: NC:winwlx.PWLX_GET_SOURCE_DESKTOP
title: PWLX_GET_SOURCE_DESKTOP
author: windows-sdk-content
description: Called by GINA to determine the name and handle of the desktop that was current before Winlogon switched to the Winlogon desktop.
old-location: security\wlxgetsourcedesktop.htm
tech.root: secauthn
ms.assetid: c0b6c64e-7c2b-4dc9-81fd-243fc2230249
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: PWLX_GET_SOURCE_DESKTOP, PWLX_GET_SOURCE_DESKTOP callback, WlxGetSourceDesktop, WlxGetSourceDesktop callback function [Security], _gina_wlxgetsourcedesktop, security.wlxgetsourcedesktop, winwlx/WlxGetSourceDesktop
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WlxGetSourceDesktop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_GET_SOURCE_DESKTOP callback function


## -description


<p class="CCE_Message">[The WlxGetSourceDesktop function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to determine the name and handle of the desktop that was current before <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> switched to the Winlogon desktop.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>GINA can use this function to modify its behavior, depending on the originating desktop.


## -parameters




### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


### -param *ppDesktop [out]

Receives a pointer to a 
<a href="https://msdn.microsoft.com/3cde1b9e-5109-400d-a67f-1e263f2283d1">WLX_DESKTOP</a> structure containing necessary information describing the desktop. This pointer can be freed with 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>.


## -returns



The <b>WlxGetSourceDesktop</b> function returns one of the following values.

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
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The call failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="https://msdn.microsoft.com/3cde1b9e-5109-400d-a67f-1e263f2283d1">WLX_DESKTOP</a>



<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

