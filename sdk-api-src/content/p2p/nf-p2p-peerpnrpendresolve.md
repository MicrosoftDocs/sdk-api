---
UID: NF:p2p.PeerPnrpEndResolve
title: PeerPnrpEndResolve function (p2p.h)
description: Closes the handle for an asynchronous PNRP resolution operation initiated with a previous call to PeerPnrpStartResolve.
helpviewer_keywords: ["PeerPnrpEndResolve","PeerPnrpEndResolve function [Peer Networking]","p2p.peerpnrpendresolve","p2p/PeerPnrpEndResolve"]
old-location: p2p\peerpnrpendresolve.htm
tech.root: p2p
ms.assetid: b700a195-57c4-481a-93d2-82d543f5c6c6
ms.date: 12/05/2018
ms.keywords: PeerPnrpEndResolve, PeerPnrpEndResolve function [Peer Networking], p2p.peerpnrpendresolve, p2p/PeerPnrpEndResolve
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
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerPnrpEndResolve
 - p2p/PeerPnrpEndResolve
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerPnrpEndResolve
---

# PeerPnrpEndResolve function


## -description

The <b>PeerPnrpEndResolve</b> function closes the handle for an asynchronous PNRP resolution operation initiated with a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpstartresolve">PeerPnrpStartResolve</a>.

## -parameters

### -param hResolve [in]

The handle to the asynchronous peer name resolution operation returned by a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpstartresolve">PeerPnrpStartResolve</a>.

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

<a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpstartresolve">PeerPnrpStartResolve</a>