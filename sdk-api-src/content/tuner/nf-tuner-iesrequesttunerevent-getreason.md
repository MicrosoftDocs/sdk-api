---
UID: NF:tuner.IESRequestTunerEvent.GetReason
title: IESRequestTunerEvent::GetReason (tuner.h)
description: Gets a code that indicates the reason a device is requesting exclusive access to a tuner and its Conditional Access Services (CAS).
helpviewer_keywords: ["GetReason","GetReason method [Microsoft TV Technologies]","GetReason method [Microsoft TV Technologies]","IESRequestTunerEvent interface","IESRequestTunerEvent interface [Microsoft TV Technologies]","GetReason method","IESRequestTunerEvent.GetReason","IESRequestTunerEvent::GetReason","mstv.iesrequesttunerevent_getreason","tuner/IESRequestTunerEvent::GetReason"]
old-location: mstv\iesrequesttunerevent_getreason.htm
tech.root: mstv
ms.assetid: ff8b9080-0299-4ba9-a49d-9ef142e91eb8
ms.date: 12/05/2018
ms.keywords: GetReason, GetReason method [Microsoft TV Technologies], GetReason method [Microsoft TV Technologies],IESRequestTunerEvent interface, IESRequestTunerEvent interface [Microsoft TV Technologies],GetReason method, IESRequestTunerEvent.GetReason, IESRequestTunerEvent::GetReason, mstv.iesrequesttunerevent_getreason, tuner/IESRequestTunerEvent::GetReason
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
 - IESRequestTunerEvent::GetReason
 - tuner/IESRequestTunerEvent::GetReason
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
 - IESRequestTunerEvent.GetReason
---

# IESRequestTunerEvent::GetReason


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a code that indicates the reason a device is requesting exclusive access to a tuner and its Conditional Access Services (CAS).

## -parameters

### -param pbyReason [out, retval]

Gets a 1-byte code that indicates the reason for the request.  The code can be any of the following values.
          

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
The requesting device needs the tuner to download an internal update, such as new firmware.
              

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