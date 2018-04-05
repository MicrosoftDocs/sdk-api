---
UID: NF:peerdist.PeerDistClientAddContentInformation
title: PeerDistClientAddContentInformation function
author: windows-driver-content
description: PeerDistClientAddContentInformation function adds the content information associated with a content handle opened by PeerDistClientOpenContent.
old-location: p2p\peerdistclientaddcontentinformation.htm
old-project: P2PSdk
ms.assetid: 933ca20c-8a28-4b6a-9ec8-85608fd02990
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PeerDistClientAddContentInformation, PeerDistClientAddContentInformation function [Peer Networking], p2p.peerdistclientaddcontentinformation, peerdist/PeerDistClientAddContentInformation
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
-	PeerDistClientAddContentInformation
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PeerDistClientAddContentInformation function


## -description


The <b>PeerDistClientAddContentInformation</b> function adds the content information associated with a content handle opened by <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param hContentHandle [in]

A <b>PEERDIST_CONTENT_HANDLE</b> opened by <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>.


### -param cbNumberOfBytes

Number of bytes in the <i>pBuffer</i> array.


### -param pBuffer [in]

Pointer to the buffer that contains the content information. This buffer must remain valid for the duration of the add operation. The caller must not use this buffer until the add operation is completed.


### -param lpOverlapped [in]

Pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure. The Internal member of <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure contains the completion status of the asynchronous operation. The Offset and OffsetHigh are reserved and must be 0.  


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
The <i>hPeerDist</i> handle is invalid.

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



In order to retrieve content data from Peer Distribution service the client must add content information that it received from the content server by calling the <b>PeerDistClientAddContentInformation</b> function. When all content information data has been added, the <a href="https://msdn.microsoft.com/0951e5e5-ad00-463e-8aa8-21b11a8acedc">PeerDistClientCompleteContentInformation</a> function must be called. Once <b>PeerDistClientCompleteContentInformation</b> is complete, the client can call <a href="https://msdn.microsoft.com/7c73e9e2-c723-4472-84e5-b0d25eb3b283">PeerDistClientStreamRead</a> or <a href="https://msdn.microsoft.com/ee64c0a8-7a07-4045-96fa-855b31c2e5b1">PeerDistClientBlockRead</a> to retrieve the data from the Peer Distribution system.

When calling this function multiple times on a single content handle, the caller must wait for each operation to complete before the next call is made.

An application is  not limited  to adding  content information with a single <b>PeerDistClientAddContentInformation</b> API call, as it is possible to add portions of that content information as it is made available. When more content information is available, the application can again call <b>PeerDistClientAddContentInformation</b>. When the application is done adding the entire content information, it must then call <a href="https://msdn.microsoft.com/0951e5e5-ad00-463e-8aa8-21b11a8acedc">PeerDistClientCompleteContentInformation</a>.





## -see-also




<a href="https://msdn.microsoft.com/0951e5e5-ad00-463e-8aa8-21b11a8acedc">PeerDistClientCompleteContentInformation</a>



<a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>



<a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>
 

 

