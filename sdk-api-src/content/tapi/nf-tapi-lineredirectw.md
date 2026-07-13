---
UID: NF:tapi.lineRedirectW
title: lineRedirectW function (tapi.h)
description: The lineRedirectW (Unicode) function (tapi.h) redirects the specified offering call to the specified destination address.
helpviewer_keywords: ["_tapi2_lineredirect", "lineRedirect", "lineRedirect function [TAPI 2.2]", "lineRedirectW", "tapi/lineRedirect", "tapi/lineRedirectW", "tapi2.lineredirect"]
old-location: tapi2\lineredirect.htm
tech.root: tapi3
ms.assetid: 014465af-26a7-451e-9d32-2e020d1043b0
ms.date: 08/09/2022
ms.keywords: _tapi2_lineredirect, lineRedirect, lineRedirect function [TAPI 2.2], lineRedirectA, lineRedirectW, tapi/lineRedirect, tapi/lineRedirectA, tapi/lineRedirectW, tapi2.lineredirect
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineRedirectW (Unicode) and lineRedirectA (ANSI)
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
 - lineRedirectW
 - tapi/lineRedirectW
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
 - lineRedirect
 - lineRedirectA
 - lineRedirectW
---

# lineRedirectW function


## -description

The 
<b>lineRedirect</b> function redirects the specified offering call to the specified destination address.

## -parameters

### -param hCall

Handle to the call to be redirected. The application must be an owner of the call. The call state of <i>hCall</i> must be <i>offering</i>.

### -param lpszDestAddress

Pointer to the destination address. This follows the standard dialable number format.

### -param dwCountryCode

Country/region code of the party the call is redirected to. If a value of 0 is specified, a default is used by the implementation.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESS, LINEERR_NOTOWNER, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALCOUNTRYCODE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM.

## -remarks

Call redirect allows an application to deflect an offering call to another address without first answering the call. Call redirect differs from call forwarding in that call forwarding is performed by the switch without the involvement of the application; redirection can be done on a call-by-call basis by the application, for example, driven by caller ID information. It differs from call transfer in that transferring a call requires the call first be answered.

After a call has been successfully redirected, the call typically transitions to idle.

Besides redirecting an incoming call, an application may have the option to accept the call using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineaccept">lineAccept</a>, reject the call using 
<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>, or answer the call using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineanswer">lineAnswer</a>. The availability of these operations is dependent on device capabilities.





> [!NOTE]
> The tapi.h header defines lineRedirect as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/redirect-ovr">Redirect overview</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineaccept">lineAccept</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineanswer">lineAnswer</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>
