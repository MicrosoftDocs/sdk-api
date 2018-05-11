---
UID: NF:peerdist.PeerDistClientAddData
title: PeerDistClientAddData function
author: windows-driver-content
description: The PeerDistClientAddData function is used to supply content to the local cache.
old-location: p2p\peerdistclientadddata.htm
old-project: P2PSdk
ms.assetid: f1fdd398-ed84-4819-b0e8-e9b653bd6848
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerDistClientAddData, PeerDistClientAddData function [Peer Networking], p2p.peerdistclientadddata, peerdist/PeerDistClientAddData
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
-	PeerDistClientAddData
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerDistClientAddData function


## -description


The <b>PeerDistClientAddData</b> function is used to supply content to the local cache.  Typically this is done when data could not be found on the local network as indicated when either <a href="https://msdn.microsoft.com/ee64c0a8-7a07-4045-96fa-855b31c2e5b1">PeerDistClientBlockRead</a> or <a href="https://msdn.microsoft.com/7c73e9e2-c723-4472-84e5-b0d25eb3b283">PeerDistClientStreamRead</a> complete with <b>ERROR_TIMEOUT</b> or <b>PEERDIST_ERROR_MISSING_DATA</b>.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param hContentHandle [in]

A <b>PEERDIST_CONTENT_HANDLE</b> returned by <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>.


### -param cbNumberOfBytes

The number of bytes to be added to the local cache.


### -param pBuffer [in]

Pointer to the buffer that contains the data to be added to the local cache. This buffer must remain valid for the duration of the add operation. The caller must not use this buffer until the add operation is completed.


### -param lpOverlapped [in]

Pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure. The byte offset from the beginning of content, at which this data is being added, is specified by setting the <b>Offset</b> and <b>OffsetHigh</b> members of the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure.  The <b>OffsetHigh</b> member MUST be set to the higher 32 bits of the byte offset and the <b>Offset</b> member MUST be set to the lower 32 bits of the byte offset.


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
The <i>hPeerDist</i> or <i>hContent</i> handle is invalid.

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
The service is unavailable.

</td>
</tr>
</table>
 




## -remarks



The data that has been added with this function and passed verification is available to other peers or hosted cache for download. The Peer Distribution service stores this data in its local cache.

If the API completes with <b>PEERDIST_ERROR_OUT_OF_BOUNDS</b>, this indicates that the offset specified in the overlapped structure is beyond the end of the content.




## -see-also




<a href="https://msdn.microsoft.com/ee64c0a8-7a07-4045-96fa-855b31c2e5b1">PeerDistClientBlockRead</a>



<a href="https://msdn.microsoft.com/7c73e9e2-c723-4472-84e5-b0d25eb3b283">PeerDistClientStreamRead</a>



<a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>
 

 

