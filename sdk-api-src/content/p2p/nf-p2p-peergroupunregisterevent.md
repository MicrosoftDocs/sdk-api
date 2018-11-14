---
UID: NF:p2p.PeerGroupUnregisterEvent
title: PeerGroupUnregisterEvent function
author: windows-sdk-content
description: The PeerGroupUnregisterEvent function unregisters a peer from notification of peer events associated with the supplied event handle.
old-location: p2p\peergroupunregisterevent.htm
tech.root: P2PSdk
ms.assetid: ad13cbf6-0dc9-4de5-aae7-2ecf6af90ea6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PeerGroupUnregisterEvent, PeerGroupUnregisterEvent function [Peer Networking], p2p.peergroupunregisterevent, p2p/PeerGroupUnregisterEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
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
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerGroupUnregisterEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PeerGroupUnregisterEvent
: 
---

# PeerGroupUnregisterEvent function


## -description


The <b>PeerGroupUnregisterEvent</b> function unregisters a peer from notification of peer events associated with the supplied event handle.


## -parameters




### -param hPeerEvent [in]

Handle returned by a previous call to <a href="https://msdn.microsoft.com/a4dc100a-d3dc-408e-a425-bded11d04db5">PeerGroupRegisterEvent</a>.  This parameter is required.


## -returns



Returns <b>S_OK</b>  if the operation succeeds. Otherwise, the function returns  the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The parameter is not valid.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks



This function must be called before the HPEEREVENT handle is closed.




## -see-also




<a href="https://msdn.microsoft.com/a4dc100a-d3dc-408e-a425-bded11d04db5">PeerGroupRegisterEvent</a>
 

 

