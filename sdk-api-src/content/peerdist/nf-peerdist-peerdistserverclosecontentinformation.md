---
UID: NF:peerdist.PeerDistServerCloseContentInformation
title: PeerDistServerCloseContentInformation function
author: windows-sdk-content
description: PeerDistServerCloseContentInformation function closes the handle opened by PeerDistServerOpenContentInformation.
old-location: p2p\peerdistserverclosecontentinformation.htm
old-project: P2PSdk
ms.assetid: 066f1856-0617-40c7-a444-9765c01b4563
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerDistServerCloseContentInformation, PeerDistServerCloseContentInformation function [Peer Networking], p2p.peerdistserverclosecontentinformation, peerdist/PeerDistServerCloseContentInformation
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
tech.root: 
req.typenames: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, *PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PeerDist.dll
api_name:
 - PeerDistServerCloseContentInformation
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: ADAM
---

# PeerDistServerCloseContentInformation function


## -description


The <b>PeerDistServerCloseContentInformation</b> function closes the handle  opened by <a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a>.


## -parameters




### -param hPeerDist [in]

The <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param hContentInfo [in]

The handle returned by <a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a>.


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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The provided <i>hPeerDist</i> or <i>hContentInfo</i> handles are invalid.

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
</table>
 




## -remarks



The <b>PeerDistServerCloseContentInformation</b> closes the <b>PEERDIST_CONTENTINFO_HANDLE</b>. Additionally, calling <b>PeerDistServerCloseContentInformation</b>  will cancel any pending operations associated with the <b>PEERDIST_CONTENTINFO_HANDLE</b>.




## -see-also




<a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a>
 

 

