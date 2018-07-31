---
UID: NF:winwlx.WlxNetworkProviderLoad
title: WlxNetworkProviderLoad function
author: windows-sdk-content
description: Winlogon calls this function to collect valid authentication and identification information.
old-location: security\wlxnetworkproviderload.htm
old-project: SecAuthN
ms.assetid: d9a39211-f876-46d8-9a7c-c6bb3ba9edfe
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WlxNetworkProviderLoad, WlxNetworkProviderLoad function [Security], _gina_wlxnetworkproviderload, security.wlxnetworkproviderload, winwlx/WlxNetworkProviderLoad
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ICONINFOEXW, *PICONINFOEXW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxNetworkProviderLoad
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlxNetworkProviderLoad function


## -description


<p class="CCE_Message">[The WlxNetworkProviderLoad function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxNetworkProviderLoad</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> calls this function to collect valid authentication and identification information.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

Pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


### -param pNprNotifyInfo [out]

Points to an 
<a href="https://msdn.microsoft.com/68098b26-c58d-45fb-aebe-780a73cded80">WLX_MPR_NOTIFY_INFO</a> structure that contains domain, user name, and password information for the user. Winlogon will use this information to provide identification and authentication information to network providers. 




The GINA is not required to return password information. Any <b>NULL</b> fields within the structure will be ignored by Winlogon. Use <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> to allocate each string; Winlogon will free them when they are no longer needed.


## -returns



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
Return <b>TRUE</b> if the user was authenticated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Return <b>FALSE</b> if the user was not authenticated.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

