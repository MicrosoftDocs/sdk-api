---
UID: NF:peerdist.PeerDistServerRetrieveContentInformation
title: PeerDistServerRetrieveContentInformation function (peerdist.h)
author: windows-sdk-content
description: PeerDistServerRetrieveContentInformation function retrieves the encoded content information associated with a handle returned by PeerDistServerOpenContentInformation.
old-location: p2p\peerdistserverretrievecontentinformation.htm
tech.root: P2PSdk
ms.assetid: 376ece5f-93ea-4650-a6d8-351ae60fc15b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerDistServerRetrieveContentInformation, PeerDistServerRetrieveContentInformation function [Peer Networking], p2p.peerdistserverretrievecontentinformation, peerdist/PeerDistServerRetrieveContentInformation
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
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PeerDist.dll
api_name:
 - PeerDistServerRetrieveContentInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerDistServerRetrieveContentInformation function


## -description


The <b>PeerDistServerRetrieveContentInformation</b> function retrieves the encoded content information associated with a handle returned by <a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a>.


## -parameters




### -param hPeerDist [in]

A PEERDIST_INSTANCE_HANDLE returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param hContentInfo [in]

The handle returned by <a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a>.


### -param cbMaxNumberOfBytes

The maximum number of bytes to read.


### -param pBuffer [in, out]

Pointer to the buffer that receives the content information data.


### -param lpOverlapped [in]

Pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure. This function does not allow the caller to specify the start Offset in the content. The offset is implicitly maintained per hContentInfo. The Offset and OffsetHigh are reserved and must be zero.


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
The <i>hPeerDist</i> or <i>hContentInfo</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_NO_MORE</b></dt>
</dl>
</td>
<td width="60%">
EOF on the content information has been reached.

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



On the success of the <b>PeerDistServerRetrieveContentInformation</b> operation, the <b>Offset</b> and <b>OffsetHigh</b> fields of the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure will be populated with the <b>ULONGLONG</b> offset in the content information that was retrieved. The <b>OffsetHigh</b> member will be set to the higher 32 bits of the offset and the <b>Offset</b> member will be set to the lower 32 bits of the offset.


<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> will populate <i>lpNumberOfBytesTransferred</i> with the number of bytes transferred. In the event the caller is using a completion port to process Peer Distribution API completions, the <i>lpNumberOfBytes</i> argument of <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> will be populated with the number of bytes transferred.




## -see-also




<a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a>



<a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>
 

 

