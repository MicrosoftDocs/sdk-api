---
UID: NF:p2p.PeerPnrpEndResolve
title: PeerPnrpEndResolve function
author: windows-sdk-content
description: Closes the handle for an asynchronous PNRP resolution operation initiated with a previous call to PeerPnrpStartResolve.
old-location: p2p\peerpnrpendresolve.htm
old-project: P2PSdk
ms.assetid: b700a195-57c4-481a-93d2-82d543f5c6c6
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: PeerPnrpEndResolve, PeerPnrpEndResolve function [Peer Networking], p2p.peerpnrpendresolve, p2p/PeerPnrpEndResolve
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PEER_WATCH_PERMISSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2P.dll
api_name:
-	PeerPnrpEndResolve
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerPnrpEndResolve function


## -description


The <b>PeerPnrpEndResolve</b> function closes the handle for an asynchronous PNRP resolution operation initiated with a previous call to <a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a>.


## -parameters




### -param hResolve [in]

The handle to the asynchronous peer name resolution operation returned by a previous call to <a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a>.


## -returns



If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform the specified operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a>
 

 

