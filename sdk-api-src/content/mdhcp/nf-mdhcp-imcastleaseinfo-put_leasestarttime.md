---
UID: NF:mdhcp.IMcastLeaseInfo.put_LeaseStartTime
title: IMcastLeaseInfo::put_LeaseStartTime
author: windows-sdk-content
description: The put_LeaseStartTime method sets the start time of the lease. This method, along with put_LeaseStopTime, allows renewal of a lease without calling IMcastAddressAllocation::CreateLeaseInfo.
old-location: tapi3\imcastleaseinfo_put_leasestarttime.htm
tech.root: tapi
ms.assetid: f101a92a-bcbb-4d96-befd-c6ee83b68481
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IMcastLeaseInfo interface [TAPI 2.2],put_LeaseStartTime method, IMcastLeaseInfo.put_LeaseStartTime, IMcastLeaseInfo::put_LeaseStartTime, _tapi3_imcastleaseinfo_put_leasestarttime, mdhcp/IMcastLeaseInfo::put_LeaseStartTime, put_LeaseStartTime, put_LeaseStartTime method [TAPI 2.2], put_LeaseStartTime method [TAPI 2.2],IMcastLeaseInfo interface, tapi3.imcastleaseinfo_put_leasestarttime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMcastLeaseInfo.put_LeaseStartTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMcastLeaseInfo::put_LeaseStartTime


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>put_LeaseStartTime</b> method sets the start time of the lease. This method, along with 
<a href="https://msdn.microsoft.com/dd171ebe-c436-46cf-9a4a-31f22acbaab2">put_LeaseStopTime</a>, allows renewal of a lease without calling 
<a href="https://msdn.microsoft.com/b7a65998-3329-4117-be91-10e2dd7047d5">IMcastAddressAllocation::CreateLeaseInfo</a>.


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




<a href="https://msdn.microsoft.com/a4ad8009-559e-4db9-9ae2-28e4d36cf346">IMcastLeaseInfo</a>



<a href="https://msdn.microsoft.com/b0998a2d-6ec5-4d39-ba75-ede352b4cbe8">get_LeaseStartTime</a>
 

 

