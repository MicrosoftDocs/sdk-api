---
UID: NF:peerdist.PeerDistGetStatusEx
title: PeerDistGetStatusEx function (peerdist.h)
description: PeerDistGetStatusEx function returns the current status and capabilities of the Peer Distribution service.
helpviewer_keywords: ["PeerDistGetStatusEx","PeerDistGetStatusEx function [Peer Networking]","p2p.peerdistgetstatusex","peerdist/PeerDistGetStatusEx"]
old-location: p2p\peerdistgetstatusex.htm
tech.root: p2p
ms.assetid: 7D8D3B84-F353-4820-B035-5F289085BE7E
ms.date: 12/05/2018
ms.keywords: PeerDistGetStatusEx, PeerDistGetStatusEx function [Peer Networking], p2p.peerdistgetstatusex, peerdist/PeerDistGetStatusEx
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerDistGetStatusEx
 - peerdist/PeerDistGetStatusEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PeerDist.h
api_name:
 - PeerDistGetStatusEx
---

# PeerDistGetStatusEx function


## -description

The <b>PeerDistGetStatusEx</b> function returns the current status and capabilities of the Peer Distribution service.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param pPeerDistStatus [in, out]

A pointer to a <a href="/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info">PEERDIST_STATUS_INFO</a> structure that contains the current status and capabilities of the Peer Distribution service.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -remarks

A Group Policy change can result in the Peer Distribution service  moving to an  available, unavailable, or disabled state. Depending on the resultant state of this transition, the content, content information, or stream handles  the caller has access to may  no longer function. If this is the case, the caller must explicitly close the handles by calling the appropriate Peer Distribution API.

## -see-also

<a href="/windows/desktop/api/peerdist/ne-peerdist-peerdist_status">PEERDIST_STATUS</a>



<a href="/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info">PEERDIST_STATUS_INFO</a>