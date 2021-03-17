---
UID: NF:tapi.lineSetCallParams
title: lineSetCallParams function (tapi.h)
description: The lineSetCallParams function allows an application to change bearer mode and/or the rate parameters of an existing call.
helpviewer_keywords: ["_tapi2_linesetcallparams","lineSetCallParams","lineSetCallParams function [TAPI 2.2]","tapi/lineSetCallParams","tapi2.linesetcallparams"]
old-location: tapi2\linesetcallparams.htm
tech.root: tapi3
ms.assetid: c8088116-2bfc-420f-a83a-d00c7947b6e7
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetcallparams, lineSetCallParams, lineSetCallParams function [TAPI 2.2], tapi/lineSetCallParams, tapi2.linesetcallparams
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
 - lineSetCallParams
 - tapi/lineSetCallParams
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
 - lineSetCallParams
---

# lineSetCallParams function


## -description

The 
<b>lineSetCallParams</b> function allows an application to change bearer mode and/or the rate parameters of an existing call.

## -parameters

### -param hCall

Handle to the call whose parameters are to be changed. The application must be an owner of the call. The call state of <i>hCall</i> can be any state except <i>idle</i> or <i>disconnected</i>.

### -param dwBearerMode

New bearer mode for the call. This parameter uses one and only one of the 
<a href="/windows/desktop/Tapi/linebearermode--constants">LINEBEARERMODE_ Constants</a>.

### -param dwMinRate

Lower bound for the call's new data rate. The application can accept a new rate as low as this one.

### -param dwMaxRate

Upper bound for the call's new data rate. This is the maximum data rate the application can accept. If an exact data rate is required, <i>dwMinRate</i> and <i>dwMaxRate</i> should be equal.

### -param lpDialParams

Pointer to the new dial parameters for the call, of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linedialparams">LINEDIALPARAMS</a>. This parameter can be left <b>NULL</b> if the call's current dialing parameters are to be used.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_BEARERMODEUNAVAIL, LINEERR_NOTOWNER, LINEERR_INVALBEARERMODE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RATEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALRATE, LINEERR_UNINITIALIZED, LINEERR_NOMEM.

## -remarks

This operation is used to change the parameters of an existing call. Examples of its usage include changing the bearer mode and/or the data rate of an existing call.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedialparams">LINEDIALPARAMS</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>