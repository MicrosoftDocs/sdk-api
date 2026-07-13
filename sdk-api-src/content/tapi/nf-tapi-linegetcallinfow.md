---
UID: NF:tapi.lineGetCallInfoW
title: lineGetCallInfoW function (tapi.h)
description: The lineGetCallInfoW (Unicode) function (tapi.h) enables an application to obtain fixed information about the specified call.
helpviewer_keywords: ["_tapi2_linegetcallinfo", "lineGetCallInfo", "lineGetCallInfo function [TAPI 2.2]", "lineGetCallInfoW", "tapi/lineGetCallInfo", "tapi/lineGetCallInfoW", "tapi2.linegetcallinfo"]
old-location: tapi2\linegetcallinfo.htm
tech.root: tapi3
ms.assetid: e69722cb-9c45-4f1a-a855-64afa3c33276
ms.date: 08/09/2022
ms.keywords: _tapi2_linegetcallinfo, lineGetCallInfo, lineGetCallInfo function [TAPI 2.2], lineGetCallInfoA, lineGetCallInfoW, tapi/lineGetCallInfo, tapi/lineGetCallInfoA, tapi/lineGetCallInfoW, tapi2.linegetcallinfo
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetCallInfoW (Unicode) and lineGetCallInfoA (ANSI)
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
 - lineGetCallInfoW
 - tapi/lineGetCallInfoW
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
 - lineGetCallInfo
 - lineGetCallInfoA
 - lineGetCallInfoW
---

# lineGetCallInfoW function


## -description

The 
<b>lineGetCallInfo</b> function enables an application to obtain fixed information about the specified call.

## -parameters

### -param hCall

Handle to the call to be queried. The call state of <i>hCall</i> can be any state.

### -param lpCallInfo

Pointer to a variably sized data structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>. Upon successful completion of the request, this structure is filled with call-related information. Prior to calling 
<b>lineGetCallInfo</b>, the application should set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL.

## -remarks

A separate 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure exists for every incoming or outgoing call. The structure contains primarily fixed information about the call. An application would typically be interested in checking this information when it receives its handle for a call by the 
<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a> message, or each time it receives notification by a 
<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a> message that parts of the call information structure have changed. These messages supply the handle for the call as a parameter.





> [!NOTE]
> The tapi.h header defines lineGetCallInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a>



<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
