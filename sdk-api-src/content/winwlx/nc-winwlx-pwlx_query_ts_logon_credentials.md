---
UID: NC:winwlx.PWLX_QUERY_TS_LOGON_CREDENTIALS
title: PWLX_QUERY_TS_LOGON_CREDENTIALS
author: windows-sdk-content
description: Called by a replacement GINA DLL to retrieve credentials information if Terminal Services is enabled. The GINA DLL can then use this information to fill in a logon box automatically and attempt to log the user in.
old-location: security\wlxquerytslogoncredentials.htm
tech.root: secauthn
ms.assetid: 1365b798-682e-4cdb-b8f5-9e7c65366154
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: PWLX_QUERY_TS_LOGON_CREDENTIALS, PWLX_QUERY_TS_LOGON_CREDENTIALS callback, WlxQueryTsLogonCredentials, WlxQueryTsLogonCredentials callback function [Security], security.wlxquerytslogoncredentials, winwlx/WlxQueryTsLogonCredentials
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
 - WlxQueryTsLogonCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_QUERY_TS_LOGON_CREDENTIALS callback function


## -description


Called by a replacement 
				<a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL to retrieve <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> information if Terminal Services is enabled.
			The GINA DLL can then use this information to fill in a logon box automatically and attempt to log the user in.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pCred [out]

When the return value is <b>TRUE</b>, <i>pCred</i> specifies a pointer to a <a href="https://msdn.microsoft.com/74783de8-9134-45d8-a8de-26aec884db4d">WLX_CLIENT_CREDENTIALS_INFO_V2_0</a> structure that contains the credentials to use for auto logon.


## -returns



The <b>WlxQueryTsLogonCredentials</b> function returns one of the following values.

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
The credentials information was retrieved and returned in <i>pCred</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The credentials information was not retrieved.

</td>
</tr>
</table>
 




## -remarks



This function supersedes the <a href="https://msdn.microsoft.com/b563606d-f4d5-48d7-914d-a11ed5f536a1">WlxQueryClientCredentials</a> and <a href="https://msdn.microsoft.com/dfa12961-1552-4531-8f79-d44fb2a46e74">WlxQueryInetConnectorCredentials</a> functions.

To access this function, the GINA DLL must use the 
<a href="https://msdn.microsoft.com/b2d0c936-5430-48ed-b808-92209b909406">WLX_DISPATCH_VERSION_1_4</a> structure and set the Winlogon version to at least WLX_VERSION_1_4 in its 
<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a> call.

Other Winlogon support functions that may be called when Terminal Services is enabled are <a href="https://msdn.microsoft.com/4f9f56dd-13cf-4125-90d0-4858a6c141be">WlxDisconnect</a>, <a href="https://msdn.microsoft.com/b563606d-f4d5-48d7-914d-a11ed5f536a1">WlxQueryClientCredentials</a>,
<a href="https://msdn.microsoft.com/a7b81d76-74de-44a8-92ad-765ad1f7013e">WlxQueryTerminalServicesData</a>, and 
<a href="https://msdn.microsoft.com/bb36254c-0696-4f3f-89d7-332837ec3a75">WlxWin31Migrate</a>.




## -see-also




<a href="https://msdn.microsoft.com/74783de8-9134-45d8-a8de-26aec884db4d">WLX_CLIENT_CREDENTIALS_INFO_V2_0</a>



<a href="https://msdn.microsoft.com/4f9f56dd-13cf-4125-90d0-4858a6c141be">WlxDisconnect</a>



<a href="https://msdn.microsoft.com/b563606d-f4d5-48d7-914d-a11ed5f536a1">WlxQueryClientCredentials</a>



<a href="https://msdn.microsoft.com/a7b81d76-74de-44a8-92ad-765ad1f7013e">WlxQueryTerminalServicesData</a>



<a href="https://msdn.microsoft.com/bb36254c-0696-4f3f-89d7-332837ec3a75">WlxWin31Migrate</a>
 

 

