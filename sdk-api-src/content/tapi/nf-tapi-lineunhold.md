---
UID: NF:tapi.lineUnhold
title: lineUnhold function (tapi.h)
description: The lineUnhold function retrieves the specified held call.
helpviewer_keywords: ["_tapi2_lineunhold","lineUnhold","lineUnhold function [TAPI 2.2]","tapi/lineUnhold","tapi2.lineunhold"]
old-location: tapi2\lineunhold.htm
tech.root: tapi3
ms.assetid: c32d8d3a-f54c-411a-ae86-4aecd6dce456
ms.date: 12/05/2018
ms.keywords: _tapi2_lineunhold, lineUnhold, lineUnhold function [TAPI 2.2], tapi/lineUnhold, tapi2.lineunhold
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
 - lineUnhold
 - tapi/lineUnhold
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
 - lineUnhold
---

# lineUnhold function


## -description

The 
<b>lineUnhold</b> function retrieves the specified held call.

## -parameters

### -param hCall

Handle to the call to be retrieved. The application must be an owner of this call. The call state of <i>hCall</i> must be <i>onHold</i>, <i>onHoldPendingTransfer</i>, or <i>onHoldPendingConference</i>.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding <a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>