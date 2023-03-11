---
UID: NF:tapi3cc.ITAgentSessionEvent.get_Session
title: ITAgentSessionEvent::get_Session (tapi3cc.h)
description: The ITAgentSessionEvent::get_Session method (tapi3cc.h) method gets a pointer to the ITAgentSession on which the event occurred.
helpviewer_keywords: ["ITAgentSessionEvent interface [TAPI 2.2]","get_Session method","ITAgentSessionEvent.get_Session","ITAgentSessionEvent::get_Session","_tapi3_itagentsessionevent_get_session","get_Session","get_Session method [TAPI 2.2]","get_Session method [TAPI 2.2]","ITAgentSessionEvent interface","tapi3.itagentsessionevent_get_session","tapi3cc/ITAgentSessionEvent::get_Session"]
old-location: tapi3\itagentsessionevent_get_session.htm
tech.root: tapi3
ms.assetid: 2868e5db-f596-424d-bd6a-0f0c5f52e1e7
ms.date: 08/10/2022
ms.keywords: ITAgentSessionEvent interface [TAPI 2.2],get_Session method, ITAgentSessionEvent.get_Session, ITAgentSessionEvent::get_Session, _tapi3_itagentsessionevent_get_session, get_Session, get_Session method [TAPI 2.2], get_Session method [TAPI 2.2],ITAgentSessionEvent interface, tapi3.itagentsessionevent_get_session, tapi3cc/ITAgentSessionEvent::get_Session
req.header: tapi3cc.h
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
 - ITAgentSessionEvent::get_Session
 - tapi3cc/ITAgentSessionEvent::get_Session
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
 - ITAgentSessionEvent.get_Session
---

# ITAgentSessionEvent::get_Session


## -description

The 
<b>get_Session</b> method gets a pointer to the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> on which the event occurred.

## -parameters

### -param ppSession [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> interface.

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
The <i>ppSession</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> interface returned by <b>ITAgentSessionEvent::get_Session</b>. The application must call <b>Release</b> on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsessionevent">ITAgentSessionEvent</a>
