---
UID: NF:p2p.PeerCollabSetEndpointName
title: PeerCollabSetEndpointName function
author: windows-sdk-content
description: Sets the name of the current endpoint used by the peer application.
old-location: p2p\peercollabsetendpointname.htm
old-project: P2PSdk
ms.assetid: 9b8d0559-c70e-4b05-bd73-1eb3b2e8f9c8
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PeerCollabSetEndpointName, PeerCollabSetEndpointName function [Peer Networking], p2p.peercollabsetendpointname, p2p/PeerCollabSetEndpointName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: PEER_WATCH_PERMISSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabSetEndpointName
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerCollabSetEndpointName function


## -description


The <b>PeerCollabSetEndpointName</b> function sets the name of the current endpoint used by the peer application.


## -parameters




### -param pwzEndpointName [in]

Pointer to the new name of the current endpoint, represented as a zero-terminated Unicode string. An error is raised if the new name is the same as the current one. An endpoint name is limited to 255 Unicode characters.


## -returns



Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_SIGNED_IN</b></dt>
</dl>
</td>
<td width="60%">
The operation requires the user to be signed in.

</td>
</tr>
</table>
 




## -remarks



An endpoint name is set to the machine name by default. However, a new endpoint name set by the <b>PeerCollabSetEndpointName</b> function will persist across reboots. 




## -see-also




<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>
 

 

