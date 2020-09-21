---
UID: NF:tapi.lineSecureCall
title: lineSecureCall function (tapi.h)
description: The lineSecureCall function secures the call from any interruptions or interference that can affect the call's media stream.
helpviewer_keywords: ["_tapi2_linesecurecall","lineSecureCall","lineSecureCall function [TAPI 2.2]","tapi/lineSecureCall","tapi2.linesecurecall"]
old-location: tapi2\linesecurecall.htm
tech.root: tapi3
ms.assetid: b12a5734-0638-4bb0-8f25-ca27d28e528b
ms.date: 12/05/2018
ms.keywords: _tapi2_linesecurecall, lineSecureCall, lineSecureCall function [TAPI 2.2], tapi/lineSecureCall, tapi2.linesecurecall
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
 - lineSecureCall
 - tapi/lineSecureCall
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
 - lineSecureCall
---

# lineSecureCall function


## -description

The 
<b>lineSecureCall</b> function secures the call from any interruptions or interference that can affect the call's media stream.

## -parameters

### -param hCall

Handle to the call to be secured. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED.

## -remarks

A call can be secured to avoid interference. For example, in an analog environment, call-waiting tones can destroy a fax or modem session on the original call. The 
<b>lineSecureCall</b> function allows an existing call to be secured. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> function provides the option to secure the call from the time of call setup. The securing of a call remains in effect for the duration of the call.

## -see-also

<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/secure-a-session-ovr">Secure a Session overview</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>