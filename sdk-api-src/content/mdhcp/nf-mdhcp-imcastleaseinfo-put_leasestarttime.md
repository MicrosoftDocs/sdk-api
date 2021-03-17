---
UID: NF:mdhcp.IMcastLeaseInfo.put_LeaseStartTime
title: IMcastLeaseInfo::put_LeaseStartTime (mdhcp.h)
description: The put_LeaseStartTime method sets the start time of the lease. This method, along with put_LeaseStopTime, allows renewal of a lease without calling IMcastAddressAllocation::CreateLeaseInfo.
helpviewer_keywords: ["IMcastLeaseInfo interface [TAPI 2.2]","put_LeaseStartTime method","IMcastLeaseInfo.put_LeaseStartTime","IMcastLeaseInfo::put_LeaseStartTime","_tapi3_imcastleaseinfo_put_leasestarttime","mdhcp/IMcastLeaseInfo::put_LeaseStartTime","put_LeaseStartTime","put_LeaseStartTime method [TAPI 2.2]","put_LeaseStartTime method [TAPI 2.2]","IMcastLeaseInfo interface","tapi3.imcastleaseinfo_put_leasestarttime"]
old-location: tapi3\imcastleaseinfo_put_leasestarttime.htm
tech.root: tapi3
ms.assetid: f101a92a-bcbb-4d96-befd-c6ee83b68481
ms.date: 12/05/2018
ms.keywords: IMcastLeaseInfo interface [TAPI 2.2],put_LeaseStartTime method, IMcastLeaseInfo.put_LeaseStartTime, IMcastLeaseInfo::put_LeaseStartTime, _tapi3_imcastleaseinfo_put_leasestarttime, mdhcp/IMcastLeaseInfo::put_LeaseStartTime, put_LeaseStartTime, put_LeaseStartTime method [TAPI 2.2], put_LeaseStartTime method [TAPI 2.2],IMcastLeaseInfo interface, tapi3.imcastleaseinfo_put_leasestarttime
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
 - IMcastLeaseInfo::put_LeaseStartTime
 - mdhcp/IMcastLeaseInfo::put_LeaseStartTime
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
 - IMcastLeaseInfo.put_LeaseStartTime
---

# IMcastLeaseInfo::put_LeaseStartTime


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>put_LeaseStartTime</b> method sets the start time of the lease. This method, along with 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-put_leasestoptime">put_LeaseStopTime</a>, allows renewal of a lease without calling 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-createleaseinfo">IMcastAddressAllocation::CreateLeaseInfo</a>.

## -parameters

### -param time [in]

A <b>DATE</b> specifying the start time of the lease.

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



<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-get_leasestarttime">get_LeaseStartTime</a>