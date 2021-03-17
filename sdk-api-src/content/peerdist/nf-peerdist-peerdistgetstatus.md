---
UID: NF:peerdist.PeerDistGetStatus
title: PeerDistGetStatus function (peerdist.h)
description: PeerDistGetStatus function returns the current status of the Peer Distribution service.
helpviewer_keywords: ["PeerDistGetStatus","PeerDistGetStatus function [Peer Networking]","p2p.peerdistgetstatus","peerdist/PeerDistGetStatus"]
old-location: p2p\peerdistgetstatus.htm
tech.root: p2p
ms.assetid: 1ab188cc-db79-49b2-977f-0b8fccf7f274
ms.date: 12/05/2018
ms.keywords: PeerDistGetStatus, PeerDistGetStatus function [Peer Networking], p2p.peerdistgetstatus, peerdist/PeerDistGetStatus
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
 - PeerDistGetStatus
 - peerdist/PeerDistGetStatus
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
 - PeerDistGetStatus
---

# PeerDistGetStatus function


## -description

The <b>PeerDistGetStatus</b> function returns the current status of the Peer Distribution service.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param pPeerDistStatus [out]

A pointer to a <a href="/windows/desktop/api/peerdist/ne-peerdist-peerdist_status">PEERDIST_STATUS</a> enumeration which upon operation success receives the current status of the Peer Distribution service.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -remarks

A Group Policy change can result in the Peer Distribution service  moving to an  available, unavailable, or disabled state. Depending on the resultant state of this transition, the content, content information, or stream handles  the caller has access to may  no longer function. If this is the case, the caller must explicitly close the handles by calling the appropriate Peer Distribution API.

## -see-also

<a href="/windows/desktop/api/peerdist/ne-peerdist-peerdist_status">PEERDIST_STATUS</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientclosecontent">PeerDistClientCloseContent</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosecontentinformation">PeerDistServerCloseContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosestreamhandle">PeerDistServerCloseStreamHandle</a>