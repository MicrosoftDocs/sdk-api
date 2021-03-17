---
UID: NF:tapi.lineRegisterRequestRecipient
title: lineRegisterRequestRecipient function (tapi.h)
description: The lineRegisterRequestRecipient function registers the invoking application as a recipient of requests for the specified request mode.
helpviewer_keywords: ["_tapi2_lineregisterrequestrecipient","lineRegisterRequestRecipient","lineRegisterRequestRecipient function [TAPI 2.2]","tapi/lineRegisterRequestRecipient","tapi2.lineregisterrequestrecipient"]
old-location: tapi2\lineregisterrequestrecipient.htm
tech.root: tapi3
ms.assetid: ff2f9ab0-389f-4b35-abd1-29486750283b
ms.date: 12/05/2018
ms.keywords: _tapi2_lineregisterrequestrecipient, lineRegisterRequestRecipient, lineRegisterRequestRecipient function [TAPI 2.2], tapi/lineRegisterRequestRecipient, tapi2.lineregisterrequestrecipient
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
 - lineRegisterRequestRecipient
 - tapi/lineRegisterRequestRecipient
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
 - lineRegisterRequestRecipient
---

# lineRegisterRequestRecipient function


## -description

The 
<b>lineRegisterRequestRecipient</b> function registers the invoking application as a recipient of requests for the specified request mode.

## -parameters

### -param hLineApp

Application's usage handle for the line portion of TAPI.

### -param dwRegistrationInstance

Application-specific <b>DWORD</b> that is passed back as a parameter of the 
<a href="/windows/desktop/Tapi/line-request">LINE_REQUEST</a> message. This message notifies the application that a request is pending. This parameter is ignored if <i>bEnable</i> is set to zero. This parameter is examined by TAPI only for registration, not for deregistration. The <i>dwRegistrationInstance</i> value used while deregistering need not match the <i>dwRegistrationInstance</i> used while registering for a request mode.

### -param dwRequestMode

Type of request for which the application registers. This parameter uses one or more of the 
<a href="/windows/desktop/Tapi/linerequestmode--constants">LINEREQUESTMODE_ Constants</a>.

### -param bEnable

If <b>TRUE</b>, the application registers the specified request modes; if <b>FALSE</b>, the application deregisters for the specified request modes.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALAPPHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALREQUESTMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.

## -remarks

A telephony-enabled application can request that a call be placed on its behalf by invoking 
<a href="/windows/desktop/api/tapi/nf-tapi-tapirequestmakecall">tapiRequestMakeCall</a>. Additionally, other applications can request that information be logged with a given call. The 
<b>tapiRequestMakeCall</b> requests are queued by TAPI, and the highest priority application that has registered to handle the request is sent a 
<a href="/windows/desktop/Tapi/line-request">LINE_REQUEST</a> message with an indication of the mode of the request that is pending. This application is typically the user's call-control application.

Next, the call-control application that receives this message invokes 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetrequest">lineGetRequest</a>, specifying the request mode and a buffer that is large enough to hold the request. The call-control application then interprets and executes the request.

The recipient application is also automatically deregistered for all requests when it does a 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/line-request">LINE_REQUEST</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetrequest">lineGetRequest</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>



<a href="/windows/desktop/api/tapi/nf-tapi-tapirequestmakecall">tapiRequestMakeCall</a>