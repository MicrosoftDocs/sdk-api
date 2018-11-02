---
UID: NC:winwlx.PWLX_DISCONNECT
title: PWLX_DISCONNECT
author: windows-sdk-content
description: Called by a replacement GINA DLL if Terminal Services is enabled. GINA calls this function to disconnect from a Terminal Services network session.
old-location: security\wlxdisconnect.htm
tech.root: secauthn
ms.assetid: 4f9f56dd-13cf-4125-90d0-4858a6c141be
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: PWLX_DISCONNECT, PWLX_DISCONNECT callback, WlxDisconnect, WlxDisconnect callback function [Security], _gina_wlxdisconnect, security.wlxdisconnect, winwlx/WlxDisconnect
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
 - WlxDisconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_DISCONNECT callback function


## -description


<p class="CCE_Message">[The WlxDisconnect function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by a replacement GINA DLL if Terminal Services is enabled. <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> calls this function to disconnect from a Terminal Services network session.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div><b>WlxDisconnect</b> allows GINA to optionally support a disconnect dialog box.


## -parameters












## -returns



The <b>WlxDisconnect</b> function returns one of the following values.

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
Terminal Services session was disconnected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Terminal Services session was not disconnected, or Terminal Services was not enabled.

</td>
</tr>
</table>
 




## -remarks



To access this function, the GINA DLL must use the 
<a href="https://msdn.microsoft.com/47e343b8-ee54-45de-98c6-0ec75b45aa90">WLX_DISPATCH_VERSION_1_3</a> structure, and set the Winlogon version to at least WLX_VERSION_1_3 in its 
<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a> call.

Other Winlogon support functions that may be called when Terminal Services is enabled are <a href="https://msdn.microsoft.com/bb36254c-0696-4f3f-89d7-332837ec3a75">WlxWin31Migrate</a>, <a href="https://msdn.microsoft.com/b563606d-f4d5-48d7-914d-a11ed5f536a1">WlxQueryClientCredentials</a>, and <a href="https://msdn.microsoft.com/dfa12961-1552-4531-8f79-d44fb2a46e74">WlxQueryInetConnectorCredentials</a>.




## -see-also




<a href="https://msdn.microsoft.com/47e343b8-ee54-45de-98c6-0ec75b45aa90">WLX_DISPATCH_VERSION_1_3</a>



<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a>



<a href="https://msdn.microsoft.com/b563606d-f4d5-48d7-914d-a11ed5f536a1">WlxQueryClientCredentials</a>



<a href="https://msdn.microsoft.com/dfa12961-1552-4531-8f79-d44fb2a46e74">WlxQueryInetConnectorCredentials</a>



<a href="https://msdn.microsoft.com/bb36254c-0696-4f3f-89d7-332837ec3a75">WlxWin31Migrate</a>
 

 

