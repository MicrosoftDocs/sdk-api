---
UID: NF:tapi.lineReleaseUserUserInfo
title: lineReleaseUserUserInfo function (tapi.h)
description: The lineReleaseUserUserInfo function informs the service provider that the application has processed the user-user information contained in the LINECALLINFO structure.
helpviewer_keywords: ["_tapi2_linereleaseuseruserinfo","lineReleaseUserUserInfo","lineReleaseUserUserInfo function [TAPI 2.2]","tapi/lineReleaseUserUserInfo","tapi2.linereleaseuseruserinfo"]
old-location: tapi2\linereleaseuseruserinfo.htm
tech.root: tapi3
ms.assetid: 35d41764-7ed6-4be3-8854-37444f2a44a8
ms.date: 12/05/2018
ms.keywords: _tapi2_linereleaseuseruserinfo, lineReleaseUserUserInfo, lineReleaseUserUserInfo function [TAPI 2.2], tapi/lineReleaseUserUserInfo, tapi2.linereleaseuseruserinfo
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
 - lineReleaseUserUserInfo
 - tapi/lineReleaseUserUserInfo
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
 - lineReleaseUserUserInfo
---

# lineReleaseUserUserInfo function


## -description

The 
<b>lineReleaseUserUserInfo</b> function informs the service provider that the application has processed the user-user information contained in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure, and that subsequently received user-user information can now be written into that structure. The service provider sends a 
<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a> message indicating LINECALLINFOSTATE_USERUSERINFO when new information is available.

## -parameters

### -param hCall

Handle to the call. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.

## -returns

Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED, LINEERR_OPERATIONUNAVAIL.

## -remarks

The 
<b>lineReleaseUserUserInfo</b> function allows the application to control the flow of incoming user-user information on an ISDN connection. When a new, complete user-user information message is received, the service provider informs the application using a 
<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a> message (specifying LINECALLINFOSTATE_USERUSERINFO). Any number of applications can examine the information (using 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a>), but the application owning the call controls when the information is released so that subsequent information can be reported. The service provider will not overwrite previous user-user information in 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> with newer information until after 
<b>lineReleaseUserUserInfo</b> has been called. It is the responsibility of the service provider to buffer subsequently received user-user information until the previous information is released by the application owning the call.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a>