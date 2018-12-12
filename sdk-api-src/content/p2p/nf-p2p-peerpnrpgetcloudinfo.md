---
UID: NF:p2p.PeerPnrpGetCloudInfo
title: PeerPnrpGetCloudInfo function
author: windows-sdk-content
description: Retrieves information on the Peer Name Resolution Protocol (PNRP) clouds in which the calling peer is participating.
old-location: p2p\peerpnrpgetcloudinfo.htm
tech.root: P2PSdk
ms.assetid: e6067973-68e3-4b0e-8a7a-ffba2ab2a971
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PeerPnrpGetCloudInfo, PeerPnrpGetCloudInfo function [Peer Networking], p2p.peerpnrpgetcloudinfo, p2p/PeerPnrpGetCloudInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerPnrpGetCloudInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerPnrpGetCloudInfo function


## -description


The <b>PeerPnrpCloudInfo</b> function retrieves information on the Peer Name Resolution Protocol (PNRP) clouds in which the calling peer is participating.


## -parameters




### -param pcNumClouds [out]

The number of PNRP clouds returned in <i>ppCloudInfo</i>.


### -param ppCloudInfo [out]

Pointer to a list of <a href="https://msdn.microsoft.com/b6121bae-22b7-4f23-ac8e-08822beef559">PEER_PNRP_CLOUD_INFO</a> structures that contain information about the PNRP clouds in which the calling peer is participating.

This data returned by this parameter must be freed by calling <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.


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




<a href="https://msdn.microsoft.com/b6121bae-22b7-4f23-ac8e-08822beef559">PEER_PNRP_CLOUD_INFO</a>
 

 

