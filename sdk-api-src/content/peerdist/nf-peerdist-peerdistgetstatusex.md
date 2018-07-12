---
UID: NF:peerdist.PeerDistGetStatusEx
title: PeerDistGetStatusEx function
author: windows-sdk-content
description: PeerDistGetStatusEx function returns the current status and capabilities of the Peer Distribution service.
old-location: p2p\peerdistgetstatusex.htm
old-project: p2psdk
ms.assetid: 7D8D3B84-F353-4820-B035-5F289085BE7E
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: PeerDistGetStatusEx, PeerDistGetStatusEx function [Peer Networking], p2p.peerdistgetstatusex, peerdist/PeerDistGetStatusEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, *PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PeerDist.h
api_name:
 - PeerDistGetStatusEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PeerDistGetStatusEx function


## -description


The <b>PeerDistGetStatusEx</b> function returns the current status and capabilities of the Peer Distribution service.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param pPeerDistStatus

TBD




#### - pPeerDistStatusInfo [in, out]

A pointer to a <a href="https://msdn.microsoft.com/6EE58EA9-BA0A-4A96-9F9C-EFAF2ABA37C6">PEERDIST_STATUS_INFO</a> structure that contains the current status and capabilities of the Peer Distribution service.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



A Group Policy change can result in the Peer Distribution service  moving to an  available, unavailable, or disabled state. Depending on the resultant state of this transition, the content, content information, or stream handles  the caller has access to may  no longer function. If this is the case, the caller must explicitly close the handles by calling the appropriate Peer Distribution API.




## -see-also




<a href="https://msdn.microsoft.com/d693dc1c-39ce-4a2b-b769-9d370abc3d3c">PEERDIST_STATUS</a>



<a href="https://msdn.microsoft.com/6EE58EA9-BA0A-4A96-9F9C-EFAF2ABA37C6">PEERDIST_STATUS_INFO</a>
 

 

