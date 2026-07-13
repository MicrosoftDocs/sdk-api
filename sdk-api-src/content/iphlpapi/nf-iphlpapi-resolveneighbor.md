---
UID: NF:iphlpapi.ResolveNeighbor
title: ResolveNeighbor function (iphlpapi.h)
description: Resolves the physical address for a neighbor IP address entry on the local computer. (ResolveNeighbor)
helpviewer_keywords: ["ResolveNeighbor","ResolveNeighbor function [IP Helper]","iphlp.resolveneighbor","iphlpapi/ResolveNeighbor"]
old-location: iphlp\resolveneighbor.htm
tech.root: IpHlp
ms.assetid: c9d902c7-6543-4811-8116-003a5153bd27
ms.date: 12/05/2018
ms.keywords: ResolveNeighbor, ResolveNeighbor function [IP Helper], iphlp.resolveneighbor, iphlpapi/ResolveNeighbor
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResolveNeighbor
 - iphlpapi/ResolveNeighbor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - ResolveNeighbor
---

# ResolveNeighbor function


## -description

<p class="CCE_Message">[<b>ResolveNeighbor</b> is no longer available for use as of Windows Vista. Instead, use <a href="/windows/desktop/api/netioapi/nf-netioapi-resolveipnetentry2">ResolveIpNetEntry2</a>.]

The 
<b>ResolveNeighbor</b> function  resolves the physical address for a neighbor IP address entry on the local computer.

## -parameters

### -param NetworkAddress [in]

A pointer to a   <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a> structure that contains the neighbor IP address entry and address family.

### -param PhysicalAddress [out]

A pointer to a byte array buffer that will receive the physical address that corresponds to the IP address specified by the <i>NetworkAddress</i> parameter if the function is successful. The length of the byte array is passed in the <i>PhysicalAddressLength</i> parameter.

### -param PhysicalAddressLength [in, out]

On input, this parameter specifies the maximum length, in bytes, of the buffer passed in the <i>PhysicalAddress</i> parameter to receive the physical address. If the function is successful, this parameter will receive the length of the physical address returned in the buffer pointed to by the <i>PhysicalAddress</i> parameter. If <b>ERROR_BUFFER_OVERFLOW</b> is returned, this parameter contains the number of bytes
        required to hold the physical address.

## -returns

The <b>ResolveNeighbor</b> function always fails and returns the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-resolveipnetentry2">ResolveIpNetEntry2</a>



<a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a>
