---
UID: NF:tapi.lineParkA
title: lineParkA function (tapi.h)
description: The linePark function parks the specified call according to the specified park mode. (lineParkA)
helpviewer_keywords: ["lineParkA", "tapi/lineParkA"]
old-location: tapi2\linepark.htm
tech.root: tapi3
ms.assetid: a6198229-a6db-43ef-9ef6-957429f270cc
ms.date: 12/05/2018
ms.keywords: _tapi2_linepark, linePark, linePark function [TAPI 2.2], lineParkA, lineParkW, tapi/linePark, tapi/lineParkA, tapi/lineParkW, tapi2.linepark
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineParkW (Unicode) and lineParkA (ANSI)
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
 - lineParkA
 - tapi/lineParkA
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
 - linePark
 - lineParkA
 - lineParkW
---

# lineParkA function


## -description

The 
<b>linePark</b> function parks the specified call according to the specified park mode.

## -parameters

### -param hCall

Handle to the call to be parked. The application must be an owner of the call. The call state of <i>hCall</i> must be <i>connected</i>.

### -param dwParkMode

Park mode with which the call is to be parked. This parameter can have only a single flag set, and uses one of the 
<a href="/windows/desktop/Tapi/lineparkmode--constants">LINEPARKMODE_ Constants</a>.

### -param lpszDirAddress

Pointer to a <b>null</b>-terminated string that indicates the address where the call is to be parked when using directed park. The address is in dialable number format. This parameter is ignored for nondirected park.

### -param lpNonDirAddress

Pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>. For nondirected park, the address where the call is parked is returned in this structure. This parameter is ignored for directed park. Within the 
<b>VARSTRING</b> structure, <b>dwStringFormat</b> must be set to STRINGFORMAT_ASCII (an ASCII string buffer containing a <b>null</b>-terminated string), and the terminating <b>NULL</b> must be accounted for in the <b>dwStringSize</b>. Prior to calling 
<b>linePark</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESS, LINEERR_NOTOWNER, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALPARKMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.

## -remarks

With directed park, the application determines the address at which it wants to park the call. With nondirected park, the switch determines the address and provides this to the application. In either case, a parked call can be unparked by specifying this address.

The parked call typically enters the <i>idle</i> state after it has been successfully parked, and the application should then deallocate its handle to the call. If the application performs a 
<a href="/windows/desktop/api/tapi/nf-tapi-lineunpark">lineUnpark</a> on the parked call, a new call handle is created for the unparked call even if the application has not deallocated its old call handle.

Some switches can remind the user after a call has been parked for some long amount of time. The application sees an <i>offering</i> call with a call reason set to <i>reminder</i>.

On a nondirected park, if the <b>dwTotalSize</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> structure does not specify a sufficient amount of memory to receive the park address, the corresponding reply message returns a LINEERR_STRUCTURETOOSMALL error value. In such cases, there is no way to retrieve the complete park address. When a LINEERR_STRUCTURETOOSMALL error value is returned, the <b>dwNeededSize</b> member of the NonDirAddress structure does not contain a valid value. If a LINEERR_STRUCTURETOOSMALL error value is received from a nondirected 
<b>linePark</b>, then increase the size of the buffer and call 
<b>linePark</b> again until it returns either success or a different LINEERR_XXX result.





> [!NOTE]
> The tapi.h header defines linePark as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/park-ovr">Park Overview</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineunpark">lineUnpark</a>
