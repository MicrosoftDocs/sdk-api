---
UID: NF:mdhcp.IMcastLeaseInfo.get_AddressCount
title: IMcastLeaseInfo::get_AddressCount (mdhcp.h)
description: The get_AddressCount method obtains the number of addresses requested or granted in this lease.
helpviewer_keywords: ["IMcastLeaseInfo interface [TAPI 2.2]","get_AddressCount method","IMcastLeaseInfo.get_AddressCount","IMcastLeaseInfo::get_AddressCount","_tapi3_imcastleaseinfo_get_addresscount","get_AddressCount","get_AddressCount method [TAPI 2.2]","get_AddressCount method [TAPI 2.2]","IMcastLeaseInfo interface","mdhcp/IMcastLeaseInfo::get_AddressCount","tapi3.imcastleaseinfo_get_addresscount"]
old-location: tapi3\imcastleaseinfo_get_addresscount.htm
tech.root: tapi3
ms.assetid: af7c6923-3859-46c0-aced-5b334a423e03
ms.date: 12/05/2018
ms.keywords: IMcastLeaseInfo interface [TAPI 2.2],get_AddressCount method, IMcastLeaseInfo.get_AddressCount, IMcastLeaseInfo::get_AddressCount, _tapi3_imcastleaseinfo_get_addresscount, get_AddressCount, get_AddressCount method [TAPI 2.2], get_AddressCount method [TAPI 2.2],IMcastLeaseInfo interface, mdhcp/IMcastLeaseInfo::get_AddressCount, tapi3.imcastleaseinfo_get_addresscount
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
 - IMcastLeaseInfo::get_AddressCount
 - mdhcp/IMcastLeaseInfo::get_AddressCount
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
 - IMcastLeaseInfo.get_AddressCount
---

# IMcastLeaseInfo::get_AddressCount


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>get_AddressCount</b> method obtains the number of addresses requested or granted in this lease.

## -parameters

### -param pCount [out]

Pointer to a <b>LONG</b> that will receive the number of addresses requested or granted in this lease.

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
</table>

## -remarks

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a>