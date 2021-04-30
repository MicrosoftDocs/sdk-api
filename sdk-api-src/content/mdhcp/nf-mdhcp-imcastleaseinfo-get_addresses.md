---
UID: NF:mdhcp.IMcastLeaseInfo.get_Addresses
title: IMcastLeaseInfo::get_Addresses (mdhcp.h)
description: The get_Addresses method obtains the collection of multicast addresses that are the subject of this lease or lease request. This method is primarily for Visual Basic and other scripting languages; C++ programmers use EnumerateAddresses instead.
helpviewer_keywords: ["IMcastLeaseInfo interface [TAPI 2.2]","get_Addresses method","IMcastLeaseInfo.get_Addresses","IMcastLeaseInfo::get_Addresses","_tapi3_imcastleaseinfo_get_addresses","get_Addresses","get_Addresses method [TAPI 2.2]","get_Addresses method [TAPI 2.2]","IMcastLeaseInfo interface","mdhcp/IMcastLeaseInfo::get_Addresses","tapi3.imcastleaseinfo_get_addresses"]
old-location: tapi3\imcastleaseinfo_get_addresses.htm
tech.root: tapi3
ms.assetid: 37dc1bc8-b3d9-4c84-8d37-89d50570d95c
ms.date: 12/05/2018
ms.keywords: IMcastLeaseInfo interface [TAPI 2.2],get_Addresses method, IMcastLeaseInfo.get_Addresses, IMcastLeaseInfo::get_Addresses, _tapi3_imcastleaseinfo_get_addresses, get_Addresses, get_Addresses method [TAPI 2.2], get_Addresses method [TAPI 2.2],IMcastLeaseInfo interface, mdhcp/IMcastLeaseInfo::get_Addresses, tapi3.imcastleaseinfo_get_addresses
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
 - IMcastLeaseInfo::get_Addresses
 - mdhcp/IMcastLeaseInfo::get_Addresses
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
 - IMcastLeaseInfo.get_Addresses
---

# IMcastLeaseInfo::get_Addresses


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>get_Addresses</b> method obtains the collection of multicast addresses that are the subject of this lease or lease request. This method is primarily for Visual Basic and other scripting languages; C++ programmers use 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses">EnumerateAddresses</a> instead.

## -parameters

### -param pVariant [out]

Pointer to a <b>VARIANT</b> receiving an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of <b>BSTR</b> strings. Each string is an IP version 4 address in dotted quad notation (for example, 10.111.222.111).

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
Not enough memory to allocate the collection.

</td>
</tr>
</table>

## -remarks

Each address is an IP version 4 address represented as a <b>BSTR</b> in dotted quad notation (for example, 10.111.222.111).

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface returned by <b>IMcastLeaseInfo::get_Addresses</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses">EnumerateAddresses</a>



<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>