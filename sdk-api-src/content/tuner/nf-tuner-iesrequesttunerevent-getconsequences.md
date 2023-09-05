---
UID: NF:tuner.IESRequestTunerEvent.GetConsequences
title: IESRequestTunerEvent::GetConsequences (tuner.h)
description: Gets a code that indicates the consequences of a device request for exclusive access to a tuner and its Conditional Access Services (CAS).
helpviewer_keywords: ["GetConsequences","GetConsequences method [Microsoft TV Technologies]","GetConsequences method [Microsoft TV Technologies]","IESRequestTunerEvent interface","IESRequestTunerEvent interface [Microsoft TV Technologies]","GetConsequences method","IESRequestTunerEvent.GetConsequences","IESRequestTunerEvent::GetConsequences","mstv.iesrequesttunerevent_getconsequences","tuner/IESRequestTunerEvent::GetConsequences"]
old-location: mstv\iesrequesttunerevent_getconsequences.htm
tech.root: mstv
ms.assetid: 39588da7-90e7-4544-b53c-0f0ddb6cd951
ms.date: 12/05/2018
ms.keywords: GetConsequences, GetConsequences method [Microsoft TV Technologies], GetConsequences method [Microsoft TV Technologies],IESRequestTunerEvent interface, IESRequestTunerEvent interface [Microsoft TV Technologies],GetConsequences method, IESRequestTunerEvent.GetConsequences, IESRequestTunerEvent::GetConsequences, mstv.iesrequesttunerevent_getconsequences, tuner/IESRequestTunerEvent::GetConsequences
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
 - IESRequestTunerEvent::GetConsequences
 - tuner/IESRequestTunerEvent::GetConsequences
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
 - IESRequestTunerEvent.GetConsequences
---

# IESRequestTunerEvent::GetConsequences


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a code that indicates the consequences of a device request for exclusive access to a tuner and its Conditional Access Services (CAS).

## -parameters

### -param pbyConsequences [out, retval]

Gets a 1-byte code indicating the consequences.  The code can be any of the following values.

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
Unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x01</b></dt>
</dl>
</td>
<td width="60%">
Reboot required. The device that is requesting exclusive access must reboot itself after it relinquishes access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>[Other]</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesrequesttunerevent">IESRequestTunerEvent</a>