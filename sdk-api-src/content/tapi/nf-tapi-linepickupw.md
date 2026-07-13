---
UID: NF:tapi.linePickupW
title: linePickupW function (tapi.h)
description: The linePickupW (Unicode) function (tapi.h) picks up a call alerting at the specified destination address and returns a call handle for the picked-up call. 
helpviewer_keywords: ["_tapi2_linepickup", "linePickup", "linePickup function [TAPI 2.2]", "linePickupW", "tapi/linePickup", "tapi/linePickupW", "tapi2.linepickup"]
old-location: tapi2\linepickup.htm
tech.root: tapi3
ms.assetid: 94773ca0-8ea4-443f-9c61-81969dd72a7a
ms.date: 08/09/2022
ms.keywords: _tapi2_linepickup, linePickup, linePickup function [TAPI 2.2], linePickupA, linePickupW, tapi/linePickup, tapi/linePickupA, tapi/linePickupW, tapi2.linepickup
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: linePickupW (Unicode) and linePickupA (ANSI)
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
 - linePickupW
 - tapi/linePickupW
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
 - linePickup
 - linePickupA
 - linePickupW
---

# linePickupW function


## -description

The 
<b>linePickup</b> function picks up a call alerting at the specified destination address and returns a call handle for the picked-up call. If invoked with <b>NULL</b> for the <i>lpszDestAddress</i> parameter, a group pickup is performed. If required by the device, <i>lpszGroupID</i> specifies the group identifier to which the alerting station belongs.

## -parameters

### -param hLine

Handle to the open line device on which a call is to be picked up.

### -param dwAddressID

Address on <i>hLine</i> at which the pickup is to be originated. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param lphCall

Pointer to a memory location where the handle to the picked up call is returned. The application is the initial sole owner of the call.

### -param lpszDestAddress

Pointer to a <b>null</b>-terminated character buffer that contains the address whose call is to be picked up. The address is in standard dialable address format.

### -param lpszGroupID

Pointer to a <b>null</b>-terminated character buffer containing the group identifier to which the alerting station belongs. This parameter is required on some switches to pick up calls outside of the current pickup group. 




The <i>lpszGroupID</i> parameter can be specified by itself with a <b>NULL</b> pointer for <i>lpszDestAddress</i>. Alternatively, <i>lpszGroupID</i> can be specified in addition to <i>lpszDestAddress</i>, if required by the device.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESS, LINEERR_NOMEM, LINEERR_INVALADDRESSID, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALGROUPID, LINEERR_OPERATIONFAILED, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED.

## -remarks

When a call has been picked up successfully, the application is notified by the 
<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a> message about call state changes. The 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure supplies information about the call that was picked up. It lists the reason for the call as <i>pickup</i>. This structure is available using 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a>.

If LINEADDRCAPFLAGS_PICKUPCALLWAIT is <b>TRUE</b>, 
<b>linePickup</b> can be used to pick up a call for which the user has audibly detected the call-waiting signal but for which the provider is unable to perform the detection. This gives the user a mechanism to "answer" a waiting call even though the service provider was unable to detect the call-waiting signal. Both <i>lpszDestAddress</i> and <i>lpszGroupID</i> pointer parameters must be <b>NULL</b> to pick up a call-waiting call. The 
<b>linePickup</b> function creates a new call handle for the waiting call and passes that handle to the user. The <i>dwAddressID</i> parameter is most often zero (particularly in single-line residential cases).

After 
<b>linePickup</b> has been used to pick up the second call, 
<a href="/windows/desktop/api/tapi/nf-tapi-lineswaphold">lineSwapHold</a> can be used to toggle between them. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a> function can be used to drop one (and toggle to the other), and so forth. If the user wants to drop the current call and pick up the second call, they should call 
<b>lineDrop</b> when they get the call-waiting beep, wait for the second call to ring, and then call 
<a href="/windows/desktop/api/tapi/nf-tapi-lineanswer">lineAnswer</a> on the new call handle. The LINEADDRFEATURE_PICKUP flag in the <b>dwAddressFeatures</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a> indicates when pickup is actually possible.





> [!NOTE]
> The tapi.h header defines linePickup as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/pickup-ovr">Pickup overview</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineanswer">lineAnswer</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineswaphold">lineSwapHold</a>
