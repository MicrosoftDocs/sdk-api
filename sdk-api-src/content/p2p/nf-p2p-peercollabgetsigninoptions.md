---
UID: NF:p2p.PeerCollabGetSigninOptions
title: PeerCollabGetSigninOptions function
author: windows-sdk-content
description: Obtains the peer's current signed-in peer collaboration network presence options.
old-location: p2p\peercollabgetsigninoptions.htm
old-project: P2PSdk
ms.assetid: 2b1452d3-2474-40c9-a913-de7e148e2d94
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerCollabGetSigninOptions, PeerCollabGetSigninOptions function [Peer Networking], p2p.peercollabgetsigninoptions, p2p/PeerCollabGetSigninOptions
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
 - PeerCollabGetSigninOptions
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerCollabGetSigninOptions function


## -description


The <b>PeerCollabGetSigninOptions</b> function obtains the peer's current signed-in peer collaboration network presence options.


## -parameters




### -param pdwSigninOptions

TBD




#### - dwSigninOptions [out]

The <a href="https://msdn.microsoft.com/00b7f57a-222d-4152-bded-93f1899692da">PEER_SIGNIN_FLAGS</a> enumeration value is returned by this function. 


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
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The application did not make a previous call to <a href="https://msdn.microsoft.com/b3f4ac2a-c722-4609-b893-c4b9667ae559">PeerCollabStartup</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_SIGNED_IN</b></dt>
</dl>
</td>
<td width="60%">
The application has not signed into the peer collaboration network with a previous call to <a href="https://msdn.microsoft.com/927cccfa-2711-439c-833f-348087927c09">PeerCollabSignIn</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/00b7f57a-222d-4152-bded-93f1899692da">PEER_SIGNIN_FLAGS</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/927cccfa-2711-439c-833f-348087927c09">PeerCollabSignIn</a>



<a href="https://msdn.microsoft.com/aa69a233-6104-47c6-a0b5-378794108623">PeerCollabSignOut</a>
 

 

