---
UID: NF:bits3_0.IBitsPeer.GetPeerName
title: IBitsPeer::GetPeerName
author: windows-sdk-content
description: Gets the server principal name that uniquely identifies the peer.
old-location: bits\ibitspeer_getpeername.htm
tech.root: bits
ms.assetid: 71cfc0a5-1f60-4e61-a706-bb9f9c5a6c76
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetPeerName, GetPeerName method [BITS], GetPeerName method [BITS],IBitsPeer interface, IBitsPeer interface [BITS],GetPeerName method, IBitsPeer.GetPeerName, IBitsPeer::GetPeerName, bits.ibitspeer_getpeername, bits3_0/IBitsPeer::GetPeerName
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Bits.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# IBitsPeer::GetPeerName


## -description


Gets the server principal name that uniquely identifies the peer.


## -parameters




### -param pName [out]

Null-terminated string that contains the server principal name of the peer. The principal name is of the form, server$.domain.suffix. Call the 
<a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function to free <i>pName</i> when done.


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




<a href="https://msdn.microsoft.com/en-us/library/Aa964270(v=VS.85).aspx">IBitsPeer</a>
 

 

