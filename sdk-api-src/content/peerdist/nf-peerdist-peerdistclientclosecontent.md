---
UID: NF:peerdist.PeerDistClientCloseContent
title: PeerDistClientCloseContent function
author: windows-sdk-content
description: PeerDistClientCloseContent function closes the content handle opened by PeerDistClientOpenContent.
old-location: p2p\peerdistclientclosecontent.htm
tech.root: P2PSdk
ms.assetid: c55300b7-13b6-42bf-b673-56a5e077416d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PeerDistClientCloseContent, PeerDistClientCloseContent function [Peer Networking], p2p.peerdistclientclosecontent, peerdist/PeerDistClientCloseContent
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
 - PeerDistClientCloseContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerDistClientCloseContent function


## -description


The <b>PeerDistClientCloseContent</b> function closes the content handle opened by <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param hContentHandle [in]

A <b>PEERDIST_CONTENT_HANDLE</b> opened  by <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>.


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
The <i>hPeerDist</i> or <i>hContent</i> handle is invalid.

</td>
</tr>
</table>
 




## -remarks



This function will cancel all pending asynchronous operations associated with the provided <i>hContentHandle</i>.

 All handles opened by the <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a> function must be closed by <b>PeerDistClientCloseContent</b>.




## -see-also




<a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>
 

 

