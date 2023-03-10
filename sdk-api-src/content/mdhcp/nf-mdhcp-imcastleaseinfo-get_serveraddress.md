---
UID: NF:mdhcp.IMcastLeaseInfo.get_ServerAddress
title: IMcastLeaseInfo::get_ServerAddress (mdhcp.h)
description: The get_ServerAddress method obtains a string representing the address of the multicast server granting this lease.
helpviewer_keywords: ["IMcastLeaseInfo interface [TAPI 2.2]","get_ServerAddress method","IMcastLeaseInfo.get_ServerAddress","IMcastLeaseInfo::get_ServerAddress","_tapi3_imcastleaseinfo_get_serveraddress","get_ServerAddress","get_ServerAddress method [TAPI 2.2]","get_ServerAddress method [TAPI 2.2]","IMcastLeaseInfo interface","mdhcp/IMcastLeaseInfo::get_ServerAddress","tapi3.imcastleaseinfo_get_serveraddress"]
old-location: tapi3\imcastleaseinfo_get_serveraddress.htm
tech.root: tapi3
ms.assetid: 15f33689-07d5-4bd9-978a-2b5d9088b2ed
ms.date: 12/05/2018
ms.keywords: IMcastLeaseInfo interface [TAPI 2.2],get_ServerAddress method, IMcastLeaseInfo.get_ServerAddress, IMcastLeaseInfo::get_ServerAddress, _tapi3_imcastleaseinfo_get_serveraddress, get_ServerAddress, get_ServerAddress method [TAPI 2.2], get_ServerAddress method [TAPI 2.2],IMcastLeaseInfo interface, mdhcp/IMcastLeaseInfo::get_ServerAddress, tapi3.imcastleaseinfo_get_serveraddress
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
 - IMcastLeaseInfo::get_ServerAddress
 - mdhcp/IMcastLeaseInfo::get_ServerAddress
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
 - IMcastLeaseInfo.get_ServerAddress
---

# IMcastLeaseInfo::get_ServerAddress


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>get_ServerAddress</b> method obtains a string representing the address of the multicast server granting this lease.

## -parameters

### -param ppAddress [out]

Pointer to a <b>BSTR</b> that will receive a string representation of the address of the server granting this request or renewal.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Server address unspecified.

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
Not enough memory exists to allocate the string.

</td>
</tr>
</table>

## -remarks

The <b>BSTR</b> string <i>ppAddress</i> is an IP version 4 address in dotted quad notation (for example, 10.111.222.111). If a lease information object does not describe a granted lease (for example, it was not returned by 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress">IMcastAddressAllocation::RequestAddress</a> or 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-renewaddress">IMcastAddressAllocation::RenewAddress</a>), the address is reported as the string "Unspecified".

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppAddress</i> parameter.
			

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a>