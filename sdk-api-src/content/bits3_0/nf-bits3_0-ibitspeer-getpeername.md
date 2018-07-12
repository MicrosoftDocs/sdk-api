---
UID: NF:bits3_0.IBitsPeer.GetPeerName
title: IBitsPeer::GetPeerName
author: windows-sdk-content
description: Gets the server principal name that uniquely identifies the peer.
old-location: bits\ibitspeer_getpeername.htm
old-project: bits
ms.assetid: 71cfc0a5-1f60-4e61-a706-bb9f9c5a6c76
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetPeerName, GetPeerName method [BITS], GetPeerName method [BITS],IBitsPeer interface, IBitsPeer interface [BITS],GetPeerName method, IBitsPeer.GetPeerName, IBitsPeer::GetPeerName, bits.ibitspeer_getpeername, bits3_0/IBitsPeer::GetPeerName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeer.GetPeerName
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBitsPeer::GetPeerName


## -description


Gets the server principal name that uniquely identifies the peer.


## -parameters




### -param pName [out]

Null-terminated string that contains the server principal name of the peer. The principal name is of the form, server$.domain.suffix. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>pName</i> when done.


## -returns



The method returns the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



The principal name ensures the unique identity of the peer computer and is the entity that Kerberos authenticates. 




## -see-also




<a href="https://msdn.microsoft.com/617b88d4-6c3e-4c33-9bfa-6d9f6f629866">IBitsPeer</a>
 

 

