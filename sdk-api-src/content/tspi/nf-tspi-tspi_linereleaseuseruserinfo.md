---
UID: NF:tspi.TSPI_lineReleaseUserUserInfo
title: TSPI_lineReleaseUserUserInfo function (tspi.h)
description: The TSPI_lineReleaseUserUserInfo function informs the service provider that the user-user information contained in the LINECALLINFO structure has been processed, and that subsequently received user-user information can now be written into that structure.
helpviewer_keywords: ["TSPI_lineReleaseUserUserInfo","TSPI_lineReleaseUserUserInfo function [TAPI 2.2]","_tspi_tspi_linereleaseuseruserinfo","tspi.tspi_linereleaseuseruserinfo","tspi/TSPI_lineReleaseUserUserInfo"]
old-location: tspi\tspi_linereleaseuseruserinfo.htm
tech.root: tapi3
ms.assetid: 3c760254-a8c0-406a-aa15-3a5a42aba2e7
ms.date: 12/05/2018
ms.keywords: TSPI_lineReleaseUserUserInfo, TSPI_lineReleaseUserUserInfo function [TAPI 2.2], _tspi_tspi_linereleaseuseruserinfo, tspi.tspi_linereleaseuseruserinfo, tspi/TSPI_lineReleaseUserUserInfo
req.header: tspi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_lineReleaseUserUserInfo
 - tspi/TSPI_lineReleaseUserUserInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineReleaseUserUserInfo
---

# TSPI_lineReleaseUserUserInfo function


## -description

The 
<b>TSPI_lineReleaseUserUserInfo</b> function informs the service provider that the user-user information contained in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure has been processed, and that subsequently received user-user information can now be written into that structure. The service provider sends a 
<a href="/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)">LINE_CALLINFO</a> message indicating LINECALLINFOSTATE_USERUSERINFO when new information is available.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The service provider's handle to the call for which user-user information is to be released. The call state of <i>hdCall</i> can be <i>any</i>.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

The 
<b>TSPI_lineReleaseUserUserInfo</b> function permits control of the flow of incoming user-user information on an ISDN connection. When a new, complete user-user information message is received, the service provider informs TAPI using a 
<a href="/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)">LINE_CALLINFO</a> message (specifying LINECALLINFOSTATE_USERUSERINFO). The user-user information and other fields in 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> can be examined by multiple calls to 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a>. The service provider must not overwrite previous user-user information in 
<b>LINECALLINFO</b> with newer information until after 
<b>TSPI_lineReleaseUserUserInfo</b> has been called. The service provider must buffer subsequently received user-user information until the previous information is released. Any remaining buffered information can be discarded when 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineclosecall">TSPI_lineCloseCall</a> is invoked.

If this function is invoked while there is no user-user information in 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>, the service provider should nevertheless return an indication of success.

For backward compatibility, TAPI automatically returns LINEERR_OPERATIONUNAVAIL if this function is invoked for a call on a line under the control of a service provider that does not export the function.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)">LINE_CALLINFO</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a>