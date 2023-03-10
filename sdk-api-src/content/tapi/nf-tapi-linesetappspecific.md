---
UID: NF:tapi.lineSetAppSpecific
title: lineSetAppSpecific function (tapi.h)
description: The lineSetAppSpecific function enables an application to set the application-specific field of the specified call's call-information record.
helpviewer_keywords: ["_tapi2_linesetappspecific","lineSetAppSpecific","lineSetAppSpecific function [TAPI 2.2]","tapi/lineSetAppSpecific","tapi2.linesetappspecific"]
old-location: tapi2\linesetappspecific.htm
tech.root: tapi3
ms.assetid: b7d51f62-3b19-4961-8d4c-a44dc8498f14
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetappspecific, lineSetAppSpecific, lineSetAppSpecific function [TAPI 2.2], tapi/lineSetAppSpecific, tapi2.linesetappspecific
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
 - lineSetAppSpecific
 - tapi/lineSetAppSpecific
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
 - lineSetAppSpecific
---

# lineSetAppSpecific function


## -description

The 
<b>lineSetAppSpecific</b> function enables an application to set the application-specific field of the specified call's call-information record.

## -parameters

### -param hCall

Handle to the call whose application-specific field needs to be set. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.

### -param dwAppSpecific

New content of the <b>dwAppSpecific</b> member for the call's 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure. This value is not interpreted by the Telephony API.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_NOTOWNER, LINEERR_OPERATIONUNAVAIL, LINEERR_OPERATIONFAILED.

## -remarks

The application-specific field in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> data structure that exists for each call is not interpreted by the Telephony API or any of its service providers. Its usage is entirely defined by the applications. The field can be read from the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> record returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a>. However, 
<b>lineSetAppSpecific</b> must be used to set the field so that changes become visible to other applications. When this field is changed, all other applications with call handles are sent a LINE_CALLINFO message with an indication that the <b>dwAppSpecific</b> member has changed.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a>