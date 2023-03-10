---
UID: NF:tapi3if.ITToneDetectionEvent.get_Call
title: ITToneDetectionEvent::get_Call (tapi3if.h)
description: The get_Call method gets a pointer to the call information interface for the call object on which the tone detection event occurred.
helpviewer_keywords: ["ITToneDetectionEvent interface [TAPI 2.2]","get_Call method","ITToneDetectionEvent.get_Call","ITToneDetectionEvent::get_Call","_tapi3_ittonedetectionevent_get_call","get_Call","get_Call method [TAPI 2.2]","get_Call method [TAPI 2.2]","ITToneDetectionEvent interface","tapi3.ittonedetectionevent_get_call","tapi3if/ITToneDetectionEvent::get_Call"]
old-location: tapi3\ittonedetectionevent_get_call.htm
tech.root: tapi3
ms.assetid: 50804e3d-ec60-44b3-ac6d-2518c96bfc64
ms.date: 12/05/2018
ms.keywords: ITToneDetectionEvent interface [TAPI 2.2],get_Call method, ITToneDetectionEvent.get_Call, ITToneDetectionEvent::get_Call, _tapi3_ittonedetectionevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITToneDetectionEvent interface, tapi3.ittonedetectionevent_get_call, tapi3if/ITToneDetectionEvent::get_Call
req.header: tapi3if.h
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
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITToneDetectionEvent::get_Call
 - tapi3if/ITToneDetectionEvent::get_Call
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITToneDetectionEvent.get_Call
---

# ITToneDetectionEvent::get_Call


## -description

The 
<b>get_Call</b> method gets a pointer to the call information interface for the call object on which the tone detection event occurred.

## -parameters

### -param ppCallInfo [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface.

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
The <i>ppCallInfo</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface returned by <b>ITToneDetectionEvent::get_Call</b>. The application must call <b>Release</b> on the 
<b>ITCallInfo</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittonedetectionevent">ITToneDetectionEvent</a>