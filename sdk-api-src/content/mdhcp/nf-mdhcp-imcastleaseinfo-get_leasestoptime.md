---
UID: NF:mdhcp.IMcastLeaseInfo.get_LeaseStopTime
title: IMcastLeaseInfo::get_LeaseStopTime (mdhcp.h)
description: The get_LeaseStopTime method obtains the stop time of the lease.helpviewer_keywords: ["IMcastLeaseInfo interface [TAPI 2.2]","get_LeaseStopTime method","IMcastLeaseInfo.get_LeaseStopTime","IMcastLeaseInfo::get_LeaseStopTime","_tapi3_imcastleaseinfo_get_leasestoptime","get_LeaseStopTime","get_LeaseStopTime method [TAPI 2.2]","get_LeaseStopTime method [TAPI 2.2]","IMcastLeaseInfo interface","mdhcp/IMcastLeaseInfo::get_LeaseStopTime","tapi3.imcastleaseinfo_get_leasestoptime"]
old-location: tapi3\imcastleaseinfo_get_leasestoptime.htm
tech.root: Tapi
ms.assetid: b2b99329-b176-4e5d-afb1-754c418e843a
ms.date: 12/05/2018
ms.keywords: IMcastLeaseInfo interface [TAPI 2.2],get_LeaseStopTime method, IMcastLeaseInfo.get_LeaseStopTime, IMcastLeaseInfo::get_LeaseStopTime, _tapi3_imcastleaseinfo_get_leasestoptime, get_LeaseStopTime, get_LeaseStopTime method [TAPI 2.2], get_LeaseStopTime method [TAPI 2.2],IMcastLeaseInfo interface, mdhcp/IMcastLeaseInfo::get_LeaseStopTime, tapi3.imcastleaseinfo_get_leasestoptime
f1_keywords:
- mdhcp/IMcastLeaseInfo.get_LeaseStopTime
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mdhcp.dll
api_name:
- IMcastLeaseInfo.get_LeaseStopTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMcastLeaseInfo::get_LeaseStopTime


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>get_LeaseStopTime</b> method obtains the stop time of the lease.


## -parameters




### -param pTime [out]

Pointer to a <b>DATE</b> that will receive the stop time of the lease.


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




<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mdhcp/nf-mdhcp-imcastleaseinfo-put_leasestoptime">put_LeaseStopTime</a>
 

 

