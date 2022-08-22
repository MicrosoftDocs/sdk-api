---
UID: NF:tapi3if.ITCallHubEvent.get_CallHub
title: ITCallHubEvent::get_CallHub (tapi3if.h)
description: The get_CallHub method returns a pointer to the ITCallHub interface on which the event occurred. (ITCallHubEvent.get_CallHub)
helpviewer_keywords: ["ITCallHubEvent interface [TAPI 2.2]","get_CallHub method","ITCallHubEvent.get_CallHub","ITCallHubEvent::get_CallHub","_tapi3_itcallhubevent_get_callhub","get_CallHub","get_CallHub method [TAPI 2.2]","get_CallHub method [TAPI 2.2]","ITCallHubEvent interface","tapi3.itcallhubevent_get_callhub","tapi3if/ITCallHubEvent::get_CallHub"]
old-location: tapi3\itcallhubevent_get_callhub.htm
tech.root: tapi3
ms.assetid: 4016f253-2a2d-4406-a1fc-7595d25c1c06
ms.date: 12/05/2018
ms.keywords: ITCallHubEvent interface [TAPI 2.2],get_CallHub method, ITCallHubEvent.get_CallHub, ITCallHubEvent::get_CallHub, _tapi3_itcallhubevent_get_callhub, get_CallHub, get_CallHub method [TAPI 2.2], get_CallHub method [TAPI 2.2],ITCallHubEvent interface, tapi3.itcallhubevent_get_callhub, tapi3if/ITCallHubEvent::get_CallHub
req.header: tapi3if.h
req.include-header: Tapi3.h
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
 - ITCallHubEvent::get_CallHub
 - tapi3if/ITCallHubEvent::get_CallHub
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
 - ITCallHubEvent.get_CallHub
---

# ITCallHubEvent::get_CallHub


## -description

The 
<b>get_CallHub</b> method returns a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a> interface on which the event occurred.

## -parameters

### -param ppCallHub [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a> interface.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCallHubState</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Tapi/callhub-object">CallHub Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent">ITCallHubEvent</a>
