---
UID: NF:tapi.lineSwapHold
title: lineSwapHold function (tapi.h)
description: The lineSwapHold function swaps the specified active call with the specified call on consultation hold.
helpviewer_keywords: ["_tapi2_lineswaphold","lineSwapHold","lineSwapHold function [TAPI 2.2]","tapi/lineSwapHold","tapi2.lineswaphold"]
old-location: tapi2\lineswaphold.htm
tech.root: tapi3
ms.assetid: 9e575c82-301c-4505-b400-faf4dc291ff8
ms.date: 12/05/2018
ms.keywords: _tapi2_lineswaphold, lineSwapHold, lineSwapHold function [TAPI 2.2], tapi/lineSwapHold, tapi2.lineswaphold
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
 - lineSwapHold
 - tapi/lineSwapHold
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
 - lineSwapHold
---

# lineSwapHold function


## -description

The 
<b>lineSwapHold</b> function swaps the specified active call with the specified call on consultation hold.

## -parameters

### -param hActiveCall

Handle to the active call. The application must be an owner of the call. The call state of <i>hActiveCall</i> must be <i>connected</i>.

### -param hHeldCall

Handle to the consultation call. The application must be an owner of the call. The call state of <i>hHeldCall</i> can be <i>onHoldPendingTransfer</i>, <i>onHoldPendingConference</i>, or <i>onHold</i>.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED.

## -remarks

Swapping the active call with the call on consultation hold allows the application to alternate or toggle between these two calls. This is typical in call waiting.

## -see-also

<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>