---
UID: NF:peerdist.PeerDistServerCloseStreamHandle
title: PeerDistServerCloseStreamHandle function (peerdist.h)
author: windows-sdk-content
description: PeerDistServerCloseStreamHandle function closes a handle returned by PeerDistServerPublishStream.
old-location: p2p\peerdistserverclosestreamhandle.htm
tech.root: P2PSdk
ms.assetid: 599b4694-3d03-4d25-9d02-313599aaaf0b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerDistServerCloseStreamHandle, PeerDistServerCloseStreamHandle function [Peer Networking], p2p.peerdistserverclosestreamhandle, peerdist/PeerDistServerCloseStreamHandle
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
 - PeerDistServerCloseStreamHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerDistServerCloseStreamHandle function


## -description


The <b>PeerDistServerCloseStreamHandle</b> function  closes a handle returned by <a href="https://msdn.microsoft.com/2133e578-f89d-4cfd-a522-12c2531babaa">PeerDistServerPublishStream</a>.


## -parameters




### -param hPeerDist [in]

A PEERDIST_INSTANCE_HANDLE returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param hStream [in]

A PEERDIST_STREAM_HANDLE returned by <a href="https://msdn.microsoft.com/2133e578-f89d-4cfd-a522-12c2531babaa">PeerDistServerPublishStream</a>.


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
</table>
 




## -remarks



The <b>PeerDistServerCloseStreamHandle</b> function call cancels all pending operations associated with <i>hStream</i>. To prevent unintended cancellation of publication and closure of the stream handle, this function should be called after the completion of <a href="https://msdn.microsoft.com/ad66025e-cc4f-49b7-9749-de97f4a55078">PeerDistServerPublishCompleteStream</a>.

<b>PeerDistServerCloseStreamHandle</b> does not remove the publication. In order to remove the publication, call <a href="https://msdn.microsoft.com/880927c4-f7d7-4c75-b371-2fe401a50b20">PeerDistServerUnpublish</a>.




## -see-also




<a href="https://msdn.microsoft.com/ad66025e-cc4f-49b7-9749-de97f4a55078">PeerDistServerPublishCompleteStream</a>



<a href="https://msdn.microsoft.com/2133e578-f89d-4cfd-a522-12c2531babaa">PeerDistServerPublishStream</a>



<a href="https://msdn.microsoft.com/880927c4-f7d7-4c75-b371-2fe401a50b20">PeerDistServerUnpublish</a>
 

 

