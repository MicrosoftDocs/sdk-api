---
UID: NF:mdhcp.IMcastAddressAllocation.ReleaseAddress
title: IMcastAddressAllocation::ReleaseAddress (mdhcp.h)
description: The ReleaseAddress method releases a lease that was obtained previously.
helpviewer_keywords: ["IMcastAddressAllocation interface [TAPI 2.2]","ReleaseAddress method","IMcastAddressAllocation.ReleaseAddress","IMcastAddressAllocation::ReleaseAddress","ReleaseAddress","ReleaseAddress method [TAPI 2.2]","ReleaseAddress method [TAPI 2.2]","IMcastAddressAllocation interface","_tapi3_imcastaddressallocation_releaseaddress","mdhcp/IMcastAddressAllocation::ReleaseAddress","tapi3.imcastaddressallocation_releaseaddress"]
old-location: tapi3\imcastaddressallocation_releaseaddress.htm
tech.root: tapi3
ms.assetid: 6b5fd18b-1b13-4e2a-9ff9-4a66212213a7
ms.date: 12/05/2018
ms.keywords: IMcastAddressAllocation interface [TAPI 2.2],ReleaseAddress method, IMcastAddressAllocation.ReleaseAddress, IMcastAddressAllocation::ReleaseAddress, ReleaseAddress, ReleaseAddress method [TAPI 2.2], ReleaseAddress method [TAPI 2.2],IMcastAddressAllocation interface, _tapi3_imcastaddressallocation_releaseaddress, mdhcp/IMcastAddressAllocation::ReleaseAddress, tapi3.imcastaddressallocation_releaseaddress
req.header: mdhcp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMcastAddressAllocation::ReleaseAddress
 - mdhcp/IMcastAddressAllocation::ReleaseAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mdhcp.dll
api_name:
 - IMcastAddressAllocation.ReleaseAddress
---

# IMcastAddressAllocation::ReleaseAddress


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ReleaseAddress</b> method releases a lease that was obtained previously.

## -parameters

### -param pReleaseRequest [in]

Pointer to the lease information interface.

## -returns

This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The caller passed in an invalid pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory exists to make the request.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastaddressallocation">IMcastAddressAllocation</a>