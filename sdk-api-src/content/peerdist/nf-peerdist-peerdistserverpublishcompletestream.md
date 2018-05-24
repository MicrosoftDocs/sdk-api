---
UID: NF:peerdist.PeerDistServerPublishCompleteStream
title: PeerDistServerPublishCompleteStream function
author: windows-driver-content
description: PeerDistServerPublishCompleteStream function completes the process of adding data to the stream.
old-location: p2p\peerdistserverpublishcompletestream.htm
old-project: P2PSdk
ms.assetid: ad66025e-cc4f-49b7-9749-de97f4a55078
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerDistServerPublishCompleteStream, PeerDistServerPublishCompleteStream function [Peer Networking], p2p.peerdistserverpublishcompletestream, peerdist/PeerDistServerPublishCompleteStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, *PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	PeerDist.dll
api_name:
-	PeerDistServerPublishCompleteStream
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerDistServerPublishCompleteStream function


## -description


The <b>PeerDistServerPublishCompleteStream</b> function completes the process of adding data to the stream.


## -parameters




### -param hPeerDist [in]

A PEERDIST_INSTANCE_HANDLE returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param hStream [in]

A PEERDIST_STREAM_HANDLE returned  by <a href="https://msdn.microsoft.com/2133e578-f89d-4cfd-a522-12c2531babaa">PeerDistServerPublishStream</a>.


### -param lpOverlapped [in]

Pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. The <b>Offset</b> and <b>OffsetHigh</b> are reserved and must be zero.


## -returns



If the function succeeds, the return value is <b>ERROR_IO_PENDING</b>. Otherwise, the function may return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hPeerDist</i> or <i>hStream</i> handle is invalid

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The operation was canceled.

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
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The service  is unavailable.

</td>
</tr>
</table>
 




## -remarks



Once this API completes successfully, <a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a> and <a href="https://msdn.microsoft.com/376ece5f-93ea-4650-a6d8-351ae60fc15b">PeerDistServerRetrieveContentInformation</a> can be used to retrieve content information.

<b>PeerDistServerPublishCompleteStream</b> does not close <i>hStream</i>. In order to close <i>hStream</i>, call <a href="https://msdn.microsoft.com/599b4694-3d03-4d25-9d02-313599aaaf0b">PeerDistServerCloseStreamHandle</a>.




## -see-also




<a href="https://msdn.microsoft.com/599b4694-3d03-4d25-9d02-313599aaaf0b">PeerDistServerCloseStreamHandle</a>



<a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a>



<a href="https://msdn.microsoft.com/296e21b9-9488-408a-b470-bbde1a18e6f0">PeerDistServerPublishAddToStream</a>



<a href="https://msdn.microsoft.com/2133e578-f89d-4cfd-a522-12c2531babaa">PeerDistServerPublishStream</a>



<a href="https://msdn.microsoft.com/376ece5f-93ea-4650-a6d8-351ae60fc15b">PeerDistServerRetrieveContentInformation</a>



<a href="https://msdn.microsoft.com/880927c4-f7d7-4c75-b371-2fe401a50b20">PeerDistServerUnpublish</a>
 

 

