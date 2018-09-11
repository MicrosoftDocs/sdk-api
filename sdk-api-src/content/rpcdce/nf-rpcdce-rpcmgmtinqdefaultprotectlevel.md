---
UID: NF:rpcdce.RpcMgmtInqDefaultProtectLevel
title: RpcMgmtInqDefaultProtectLevel function
author: windows-sdk-content
description: The RpcMgmtInqDefaultProtectLevel function returns the default authentication level for an authentication service.
old-location: rpc\rpcmgmtinqdefaultprotectlevel.htm
tech.root: Rpc
ms.assetid: 54a960dd-7dfc-4364-8ae8-e18fa30a51a3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RpcMgmtInqDefaultProtectLevel, RpcMgmtInqDefaultProtectLevel function [RPC], _rpc_rpcmgmtinqdefaultprotectlevel, rpc.rpcmgmtinqdefaultprotectlevel, rpcdce/RpcMgmtInqDefaultProtectLevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcMgmtInqDefaultProtectLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcMgmtInqDefaultProtectLevel function


## -description


The 
<b>RpcMgmtInqDefaultProtectLevel</b> function returns the default authentication level for an authentication service.


## -parameters




### -param AuthnSvc

Authentication service for which to return the default authentication level. Valid values are the constant for any valid security provider.


### -param AuthnLevel

Returns the default authentication level for the specified authentication service. The authentication level determines the degree to which authenticated communications between the client and server are protected. For more information, see 
<a href="https://msdn.microsoft.com/b8bb2517-e1a0-4607-a672-259f8686fc3e">Authentication Level Constants</a>. 



					


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNKNOWN_AUTH_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
Unknown authentication service.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls the 
<b>RpcMgmtInqDefaultProtectLevel</b> function to obtain the default authentication level for a specified authentication service.




## -see-also




<a href="https://msdn.microsoft.com/e7bb9955-68a7-49fe-bcdb-2450518ffe0a">RpcMgmtInqComTimeout</a>



<a href="https://msdn.microsoft.com/f6d89f2c-ff51-44ab-9f8a-2f76cd3ac6db">RpcMgmtInqIfIds</a>
 

 

