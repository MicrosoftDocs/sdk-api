---
UID: NF:mdhcp.IMcastLeaseInfo.get_RequestID
title: IMcastLeaseInfo::get_RequestID (mdhcp.h)
description: The get_RequestID method obtains the request ID for a lease.
helpviewer_keywords: ["IMcastLeaseInfo interface [TAPI 2.2]","get_RequestID method","IMcastLeaseInfo.get_RequestID","IMcastLeaseInfo::get_RequestID","_tapi3_imcastleaseinfo_get_requestid","get_RequestID","get_RequestID method [TAPI 2.2]","get_RequestID method [TAPI 2.2]","IMcastLeaseInfo interface","mdhcp/IMcastLeaseInfo::get_RequestID","tapi3.imcastleaseinfo_get_requestid"]
old-location: tapi3\imcastleaseinfo_get_requestid.htm
tech.root: tapi3
ms.assetid: 832bf532-4779-4066-a630-9892ad746a6c
ms.date: 12/05/2018
ms.keywords: IMcastLeaseInfo interface [TAPI 2.2],get_RequestID method, IMcastLeaseInfo.get_RequestID, IMcastLeaseInfo::get_RequestID, _tapi3_imcastleaseinfo_get_requestid, get_RequestID, get_RequestID method [TAPI 2.2], get_RequestID method [TAPI 2.2],IMcastLeaseInfo interface, mdhcp/IMcastLeaseInfo::get_RequestID, tapi3.imcastleaseinfo_get_requestid
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
 - IMcastLeaseInfo::get_RequestID
 - mdhcp/IMcastLeaseInfo::get_RequestID
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
 - IMcastLeaseInfo.get_RequestID
---

# IMcastLeaseInfo::get_RequestID


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>get_RequestID</b> method obtains the request ID for a lease. The primary purpose of this method is to allow you to save the request ID after your application exits, so that you can call 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-createleaseinfo">IMcastAddressAllocation::CreateLeaseInfo</a> to re-create the lease information object during a subsequent run. This allows you to renew or release a lease after the instance of your program that originally requested the lease has exited.

## -parameters

### -param ppRequestID [out]

Pointer to a <b>BSTR</b> that will receive the request ID for this lease. The request ID uniquely identifies this lease request to the server.

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
<dt><b>S_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The lease information object contains an invalid request ID.

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
Not enough memory to allocate the <b>BSTR</b>.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppRequestID</i> parameter.
			

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a>