---
UID: NF:mdhcp.IMcastLeaseInfo.get_LeaseStartTime
title: IMcastLeaseInfo::get_LeaseStartTime (mdhcp.h)
description: The get_LeaseStartTime method obtains the start time of the lease.
helpviewer_keywords: ["IMcastLeaseInfo interface [TAPI 2.2]","get_LeaseStartTime method","IMcastLeaseInfo.get_LeaseStartTime","IMcastLeaseInfo::get_LeaseStartTime","_tapi3_imcastleaseinfo_get_leasestarttime","get_LeaseStartTime","get_LeaseStartTime method [TAPI 2.2]","get_LeaseStartTime method [TAPI 2.2]","IMcastLeaseInfo interface","mdhcp/IMcastLeaseInfo::get_LeaseStartTime","tapi3.imcastleaseinfo_get_leasestarttime"]
old-location: tapi3\imcastleaseinfo_get_leasestarttime.htm
tech.root: tapi3
ms.assetid: b0998a2d-6ec5-4d39-ba75-ede352b4cbe8
ms.date: 12/05/2018
ms.keywords: IMcastLeaseInfo interface [TAPI 2.2],get_LeaseStartTime method, IMcastLeaseInfo.get_LeaseStartTime, IMcastLeaseInfo::get_LeaseStartTime, _tapi3_imcastleaseinfo_get_leasestarttime, get_LeaseStartTime, get_LeaseStartTime method [TAPI 2.2], get_LeaseStartTime method [TAPI 2.2],IMcastLeaseInfo interface, mdhcp/IMcastLeaseInfo::get_LeaseStartTime, tapi3.imcastleaseinfo_get_leasestarttime
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
 - IMcastLeaseInfo::get_LeaseStartTime
 - mdhcp/IMcastLeaseInfo::get_LeaseStartTime
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
 - IMcastLeaseInfo.get_LeaseStartTime
---

# IMcastLeaseInfo::get_LeaseStartTime


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>get_LeaseStartTime</b> method obtains the start time of the lease.

## -parameters

### -param pTime [out]

Pointer to a <b>DATE</b> that will receive the start time of the lease.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Format conversion failed for the start time or stop time.

</td>
</tr>
</table>

## -remarks

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a>



<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-put_leasestarttime">IMcastLeaseInfo::put_LeaseStartTime</a>