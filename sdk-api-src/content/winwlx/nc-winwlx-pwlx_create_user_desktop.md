---
UID: NC:winwlx.PWLX_CREATE_USER_DESKTOP
title: PWLX_CREATE_USER_DESKTOP
author: windows-sdk-content
description: Called by GINA to create alternate application desktops for the user.
old-location: security\wlxcreateuserdesktop.htm
tech.root: secauthn
ms.assetid: 6985e858-f914-426a-91b4-cf8c3f604318
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: PWLX_CREATE_USER_DESKTOP, PWLX_CREATE_USER_DESKTOP callback, WLX_CREATE_INSTANCE_ONLY, WLX_CREATE_USER, WlxCreateUserDesktop, WlxCreateUserDesktop callback function [Security], _gina_wlxcreateuserdesktop, security.wlxcreateuserdesktop, winwlx/WlxCreateUserDesktop
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
 - WlxCreateUserDesktop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_CREATE_USER_DESKTOP callback function


## -description


<p class="CCE_Message">[The WlxCreateUserDesktop function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to create alternate application desktops for the user.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


### -param hToken [in]

Specifies the handle to the token of the user for whom the desktop is being created.


### -param Flags [in]

Specifies access to the desktop. Specify one of the following. 




<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLX_CREATE_INSTANCE_ONLY"></a><a id="wlx_create_instance_only"></a><dl>
<dt><b>WLX_CREATE_INSTANCE_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Specifies that only this instance of the user has access.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_CREATE_USER"></a><a id="wlx_create_user"></a><dl>
<dt><b>WLX_CREATE_USER</b></dt>
</dl>
</td>
<td width="60%">
Specifies that any instance of this user has access.

</td>
</tr>
</table>
 


### -param pszDesktopName [in]

Specifies the name of the desktop to be created.


### -param *ppDesktop [out]

If the desktop is created, returns a pointer to a 
<a href="https://msdn.microsoft.com/3cde1b9e-5109-400d-a67f-1e263f2283d1">WLX_DESKTOP</a> structure for the new desktop. This pointer can be used in a call to 
<a href="https://msdn.microsoft.com/539e81d9-6362-4476-bdbc-849fb905b268">WlxSetReturnDesktop</a> to make this the current desktop after a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">SAS</a> event is processed.


## -returns



The <b>WlxCreateUserDesktop</b> function returns one of the following values.

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
The desktop has been created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The desktop has not been created.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>



<a href="https://msdn.microsoft.com/539e81d9-6362-4476-bdbc-849fb905b268">WlxSetReturnDesktop</a>
 

 

