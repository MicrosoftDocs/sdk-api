---
UID: NF:peerdist.PeerDistClientCompleteContentInformation
title: PeerDistClientCompleteContentInformation function
author: windows-sdk-content
description: PeerDistClientCompleteContentInformation function completes the process of adding the content information.
old-location: p2p\peerdistclientcompletecontentinformation.htm
old-project: P2PSdk
ms.assetid: 0951e5e5-ad00-463e-8aa8-21b11a8acedc
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerDistClientCompleteContentInformation, PeerDistClientCompleteContentInformation function [Peer Networking], p2p.peerdistclientcompletecontentinformation, peerdist/PeerDistClientCompleteContentInformation
ms.prod: windows
ms.technology: windows-sdk
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
-	PeerDistClientCompleteContentInformation
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerDistClientCompleteContentInformation function


## -description


The <b>PeerDistClientCompleteContentInformation</b> function  completes the process of adding the content information.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param hContentHandle [in]

A <b>PEERDIST_CONTENT_HANDLE</b> returned by <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>.


### -param lpOverlapped [in]

Pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure.


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



Upon completion of this function, a client can call <a href="https://msdn.microsoft.com/7c73e9e2-c723-4472-84e5-b0d25eb3b283">PeerDistClientStreamRead</a> or <a href="https://msdn.microsoft.com/ee64c0a8-7a07-4045-96fa-855b31c2e5b1">PeerDistClientBlockRead</a> to retrieve the data from the Peer Distribution system.




## -see-also




<a href="https://msdn.microsoft.com/933ca20c-8a28-4b6a-9ec8-85608fd02990">PeerDistClientAddContentInformation</a>



<a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>



<a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>
 

 

