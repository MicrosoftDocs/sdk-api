---
UID: NF:tapi.lineGetProxyStatus
title: lineGetProxyStatus function (tapi.h)
description: The lineGetProxyStatus function returns a list of proxy request types that are currently being serviced for the specified device.
helpviewer_keywords: ["_tapi2_linegetproxystatus","lineGetProxyStatus","lineGetProxyStatus function [TAPI 2.2]","tapi/lineGetProxyStatus","tapi2.linegetproxystatus"]
old-location: tapi2\linegetproxystatus.htm
tech.root: tapi3
ms.assetid: 0684f52f-13dd-4734-9242-acd03f7a25ae
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetproxystatus, lineGetProxyStatus, lineGetProxyStatus function [TAPI 2.2], tapi/lineGetProxyStatus, tapi2.linegetproxystatus
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
 - lineGetProxyStatus
 - tapi/lineGetProxyStatus
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
 - lineGetProxyStatus
---

# lineGetProxyStatus function


## -description

The 
<b>lineGetProxyStatus</b> function returns a list of proxy request types that are currently being serviced for the specified device.

## -parameters

### -param hLineApp

Handle to the application's registration with TAPI.

### -param dwDeviceID

Line device to be queried.

### -param dwAppAPIVersion

Version number of TAPI to be used.

### -param lpLineProxyReqestList

Pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequestlist">LINEPROXYREQUESTLIST</a>. Upon successful completion of the request, this structure is filled with a list of the currently supported proxy requests. Prior to calling 
<b>lineGetProxyStatus</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic.</div>
<div> </div>

## -returns

Returns zero if the request succeeds; otherwise, the function returns one of the following negative error values:

LINEERR_BADDEVICEID, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequestlist">LINEPROXYREQUESTLIST</a>