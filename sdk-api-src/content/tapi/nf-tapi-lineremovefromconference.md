---
UID: NF:tapi.lineRemoveFromConference
title: lineRemoveFromConference function (tapi.h)
description: The lineRemoveFromConference function removes the specified call from the conference call to which it currently belongs. The remaining calls in the conference call are unaffected.
helpviewer_keywords: ["_tapi2_lineremovefromconference","lineRemoveFromConference","lineRemoveFromConference function [TAPI 2.2]","tapi/lineRemoveFromConference","tapi2.lineremovefromconference"]
old-location: tapi2\lineremovefromconference.htm
tech.root: tapi3
ms.assetid: 03363579-66c2-4bb5-b110-01084c20bf09
ms.date: 12/05/2018
ms.keywords: _tapi2_lineremovefromconference, lineRemoveFromConference, lineRemoveFromConference function [TAPI 2.2], tapi/lineRemoveFromConference, tapi2.lineremovefromconference
req.header: tapi.h
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineRemoveFromConference
 - tapi/lineRemoveFromConference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineRemoveFromConference
---

# lineRemoveFromConference function


## -description

The 
<b>lineRemoveFromConference</b> function removes the specified call from the conference call to which it currently belongs. The remaining calls in the conference call are unaffected.

## -parameters

### -param hCall

Handle to the call to be removed from the conference. The application must be an owner of this call. The call state of <i>hCall</i> must be <i>conferenced</i>.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED.

## -remarks

This operation removes a party that currently belongs to a conference call. After the call has been successfully removed, it may be possible to further manipulate it using its handle. The availability of this operation and its result are likely to be limited in many implementations. For example, in many implementations, only the most recently added party can be removed from a conference, and the removed call can be automatically dropped (becomes idle). Consult the line's device capabilities to determine the available effects of removing a call from a conference.

If the removal of a participant from a conference is supported, the participant call, after it is removed from the conference, enters the call-state listed in the <b>dwRemoveFromConfState</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>.

## -see-also

<a href="/windows/desktop/Tapi/conference-ovr">Conference overview</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>