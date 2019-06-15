---
UID: NF:rpcdce.UuidCreateSequential
title: UuidCreateSequential function (rpcdce.h)
author: windows-sdk-content
description: The UuidCreateSequential function creates a new UUID.
old-location: rpc\uuidcreatesequential.htm
tech.root: Rpc
ms.assetid: 66975d82-559c-4a13-846c-e403b015563b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UuidCreateSequential, UuidCreateSequential function [RPC], _rpc_uuidcreatesequential, rpc.uuidcreatesequential, rpcdce/UuidCreateSequential
ms.topic: function
f1_keywords: ["rpcdce/UuidCreateSequential"]
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - UuidCreateSequential
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UuidCreateSequential function


## -description


The 
<b>UuidCreateSequential</b> function creates a new 
<a href="https://docs.microsoft.com/previous-versions/aa379358(v=vs.80)">UUID</a>.


## -parameters




### -param Uuid

Returns a pointer to the created <a href="https://docs.microsoft.com/previous-versions/aa379358(v=vs.80)">UUID</a>.


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
<dt><b>RPC_S_UUID_LOCAL_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/previous-versions/aa379358(v=vs.80)">UUID</a> is guaranteed to be unique to this computer only. For more information please see: <a href="http://support.microsoft.com/kb/981080">KB article 981080</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UUID_NO_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
Cannot get Ethernet or token-ring hardware address for this computer.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>



## -remarks



For security reasons, 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a> was modified so that it no longer uses a machine's MAC address to generate <a href="https://docs.microsoft.com/previous-versions/aa379358(v=vs.80)">UUID</a>s. 
<b>UuidCreateSequential</b> was introduced to allow creation of <b>UUID</b>s using the MAC address of a machine's Ethernet card.

The 
<b>UuidCreateSequential</b> function returns RPC_S_UUID_LOCAL_ONLY when the originating computer does not have an ethernet/token ring (IEEE 802.<i>x</i>) address. In this case, the generated <a href="https://docs.microsoft.com/previous-versions/aa379358(v=vs.80)">UUID</a> is a valid identifier, and is guaranteed to be unique among all <b>UUID</b>s generated on the computer. However, the possibility exists that another computer without an ethernet/token ring address generated the identical <b>UUID</b>. Therefore you should never use this <b>UUID</b> to identify an object that is not strictly local to your computer. Computers with ethernet/token ring addresses generate <b>UUID</b>s that are guaranteed to be globally unique.

<div class="alert"><b>Note</b>  The 
<b>UuidCreateSequential</b> function tends to be slightly faster than the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a> function. When the performance of the generation of a <a href="https://docs.microsoft.com/previous-versions/aa379358(v=vs.80)">UUID</a> is a significant consideration, the 
<b>UuidCreateSequential</b> function may be used.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-uuidfromstring">UuidFromString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring">UuidToString</a>
 

 

