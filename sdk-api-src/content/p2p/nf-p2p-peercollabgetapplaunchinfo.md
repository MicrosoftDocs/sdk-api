---
UID: NF:p2p.PeerCollabGetAppLaunchInfo
title: PeerCollabGetAppLaunchInfo function (p2p.h)
description: Obtains the peer application launch information, including the contact name, the peer endpoint, and the invitation request.
helpviewer_keywords: ["PeerCollabGetAppLaunchInfo","PeerCollabGetAppLaunchInfo function [Peer Networking]","p2p.peercollabgetapplaunchinfo","p2p/PeerCollabGetAppLaunchInfo"]
old-location: p2p\peercollabgetapplaunchinfo.htm
tech.root: p2p
ms.assetid: 266a7d80-b4bc-42f2-ba76-a69cab9e2c12
ms.date: 12/05/2018
ms.keywords: PeerCollabGetAppLaunchInfo, PeerCollabGetAppLaunchInfo function [Peer Networking], p2p.peercollabgetapplaunchinfo, p2p/PeerCollabGetAppLaunchInfo
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - PeerCollabGetAppLaunchInfo
 - p2p/PeerCollabGetAppLaunchInfo
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
 - PeerCollabGetAppLaunchInfo
---

# PeerCollabGetAppLaunchInfo function


## -description

The <b>PeerCollabGetAppLaunchInfo</b> function obtains the peer application launch information, including the contact name, the peer endpoint, and the invitation request.

## -parameters

### -param ppLaunchInfo [out]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_app_launch_info">PEER_APP_LAUNCH_INFO</a> structure that receives the peer application launch data.

Free the memory associated with this structure by passing it to <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

## -returns

Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested data does not exist.

</td>
</tr>
</table>

## -remarks

When an application invite is accepted, the application is launched with  the information sent as part of the application invite. This information can be obtained by calling <b>PeerCollabGetAppLaunchInfo</b>.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_app_launch_info">PEER_APP_LAUNCH_INFO</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>