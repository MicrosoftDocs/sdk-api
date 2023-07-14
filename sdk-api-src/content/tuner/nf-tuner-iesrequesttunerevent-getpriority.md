---
UID: NF:tuner.IESRequestTunerEvent.GetPriority
title: IESRequestTunerEvent::GetPriority (tuner.h)
description: Gets a code that indicates the priority of a device request for exclusive access to a tuner and its Conditional Access Services (CAS).
helpviewer_keywords: ["GetPriority","GetPriority method [Microsoft TV Technologies]","GetPriority method [Microsoft TV Technologies]","IESRequestTunerEvent interface","IESRequestTunerEvent interface [Microsoft TV Technologies]","GetPriority method","IESRequestTunerEvent.GetPriority","IESRequestTunerEvent::GetPriority","mstv.iesrequesttunerevent_getpriority","tuner/IESRequestTunerEvent::GetPriority"]
old-location: mstv\iesrequesttunerevent_getpriority.htm
tech.root: mstv
ms.assetid: a0edc656-0628-4020-bf8e-a5cd0bedd7c3
ms.date: 12/05/2018
ms.keywords: GetPriority, GetPriority method [Microsoft TV Technologies], GetPriority method [Microsoft TV Technologies],IESRequestTunerEvent interface, IESRequestTunerEvent interface [Microsoft TV Technologies],GetPriority method, IESRequestTunerEvent.GetPriority, IESRequestTunerEvent::GetPriority, mstv.iesrequesttunerevent_getpriority, tuner/IESRequestTunerEvent::GetPriority
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IESRequestTunerEvent::GetPriority
 - tuner/IESRequestTunerEvent::GetPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESRequestTunerEvent.GetPriority
---

# IESRequestTunerEvent::GetPriority


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a code that indicates the priority of a device request for exclusive access to a tuner and its Conditional Access Services (CAS).

## -parameters

### -param pbyPriority [out, retval]

Gets a 1-byte code that indicates the priority. The code can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x00</b></dt>
</dl>
</td>
<td width="60%">
OPPORTUNISTIC.  The device that receives the request should see if the request conflicts with any other tuner usage, including scheduled and live viewing usages.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x01</b></dt>
</dl>
</td>
<td width="60%">
NOTIFY.  The device that receives the request should check to see if the request conflicts with any other scheduled usage.  If the acquisition conflicts with live viewing, the device should prompt the user before relinquishing access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x02-0xFE</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0xFF</b></dt>
</dl>
</td>
<td width="60%">
IMMEDIATE.  The device that receives the request must release the tuner for the requestor ownership within the next 60 seconds.   The requestor can forcibly acquire the tuner after 60 seconds. 

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesrequesttunerevent">IESRequestTunerEvent</a>