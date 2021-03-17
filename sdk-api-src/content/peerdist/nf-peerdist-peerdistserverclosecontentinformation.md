---
UID: NF:peerdist.PeerDistServerCloseContentInformation
title: PeerDistServerCloseContentInformation function (peerdist.h)
description: PeerDistServerCloseContentInformation function closes the handle opened by PeerDistServerOpenContentInformation.
helpviewer_keywords: ["PeerDistServerCloseContentInformation","PeerDistServerCloseContentInformation function [Peer Networking]","p2p.peerdistserverclosecontentinformation","peerdist/PeerDistServerCloseContentInformation"]
old-location: p2p\peerdistserverclosecontentinformation.htm
tech.root: p2p
ms.assetid: 066f1856-0617-40c7-a444-9765c01b4563
ms.date: 12/05/2018
ms.keywords: PeerDistServerCloseContentInformation, PeerDistServerCloseContentInformation function [Peer Networking], p2p.peerdistserverclosecontentinformation, peerdist/PeerDistServerCloseContentInformation
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerDistServerCloseContentInformation
 - peerdist/PeerDistServerCloseContentInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PeerDist.dll
api_name:
 - PeerDistServerCloseContentInformation
---

# PeerDistServerCloseContentInformation function


## -description

The <b>PeerDistServerCloseContentInformation</b> function closes the handle  opened by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformation">PeerDistServerOpenContentInformation</a>.

## -parameters

### -param hPeerDist [in]

The <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hContentInfo [in]

The handle returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformation">PeerDistServerOpenContentInformation</a>.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function may return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The provided <i>hPeerDist</i> or <i>hContentInfo</i> handles are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DISABLED_BY_POLICY</b></dt>
</dl>
</td>
<td width="60%">
The feature is disabled by Group Policy.

</td>
</tr>
</table>

## -remarks

The <b>PeerDistServerCloseContentInformation</b> closes the <b>PEERDIST_CONTENTINFO_HANDLE</b>. Additionally, calling <b>PeerDistServerCloseContentInformation</b>  will cancel any pending operations associated with the <b>PEERDIST_CONTENTINFO_HANDLE</b>.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformation">PeerDistServerOpenContentInformation</a>