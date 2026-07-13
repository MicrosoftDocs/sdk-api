---
UID: NF:tapi.lineForwardW
title: lineForwardW function (tapi.h)
description: The lineForwardW (Unicode) function forwards calls destined for the specified address on the specified line, according to the specified forwarding instructions.
helpviewer_keywords: ["_tapi2_lineforward", "lineForward", "lineForward function [TAPI 2.2]", "lineForwardW", "tapi/lineForward", "tapi/lineForwardW", "tapi2.lineforward"]
old-location: tapi2\lineforward.htm
tech.root: tapi3
ms.assetid: 68dc99c5-1158-4e18-8e32-08216ff3567b
ms.date: 08/09/2022
ms.keywords: _tapi2_lineforward, lineForward, lineForward function [TAPI 2.2], lineForwardA, lineForwardW, tapi/lineForward, tapi/lineForwardA, tapi/lineForwardW, tapi2.lineforward
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineForwardW (Unicode) and lineForwardA (ANSI)
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
 - lineForwardW
 - tapi/lineForwardW
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
 - lineForward
 - lineForwardA
 - lineForwardW
---

# lineForwardW function


## -description

The 
<b>lineForward</b> function forwards calls destined for the specified address on the specified line, according to the specified forwarding instructions. When an originating address (<i>dwAddressID</i>) is forwarded, the specified incoming calls for that address are deflected to the other number by the switch. This function provides a combination of forward and do-not-disturb features. This function can also cancel forwarding currently in effect.

## -parameters

### -param hLine

Handle to the line device.

### -param bAllAddresses

Specifies whether all originating addresses on the line or just the one specified is to be forwarded. If <b>TRUE</b>, all addresses on the line are forwarded and <i>dwAddressID</i> is ignored; if <b>FALSE</b>, only the address specified as <i>dwAddressID</i> is forwarded.

### -param dwAddressID

Address on the specified line whose incoming calls are to be forwarded. This parameter is ignored if <i>bAllAddresses</i> is <b>TRUE</b>. 




An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param lpForwardList

Pointer to a variably sized data structure that describes the specific forwarding instructions, of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineforwardlist">LINEFORWARDLIST</a>.

### -param dwNumRingsNoAnswer

Number of rings before a call is considered a "no answer." If <i>dwNumRingsNoAnswer</i> is out of range, the actual value is set to the nearest value in the allowable range.

### -param lphConsultCall

Pointer to an HCALL location. In some telephony environments, this location is loaded with a handle to a consultation call that is used to consult the party that is being forwarded to, and the application becomes the initial sole owner of this call. This pointer must be valid even in environments where call forwarding does not require a consultation call. This handle is set to <b>NULL</b> if no consultation call is created.

### -param lpCallParams

Pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>. This pointer is ignored unless 
<b>lineForward</b> requires the establishment of a call to the forwarding destination (and <i>lphConsultCall</i> is returned, in which case <i>lpCallParams</i> is optional). If <b>NULL</b>, default call parameters are used. Otherwise, the specified call parameters are used for establishing <i>hConsultCall</i>.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_NOMEM, LINEERR_INVALADDRESSID, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESS, LINEERR_OPERATIONFAILED, LINEERR_INVALCOUNTRYCODE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALPARAM, LINEERR_UNINITIALIZED.

## -remarks

A successful forwarding indicates only that the request has been accepted by the service provider, not that forwarding is set up at the switch. A 
<a href="/windows/desktop/Tapi/line-addressstate">LINE_ADDRESSSTATE</a> (forwarding) message provides confirmation for forwarding having been set up at the switch.

Forwarding of the address(es) remains in effect until this function is called again. The most recent forwarding list replaces the old one. Forwarding can be canceled by specifying a <b>NULL</b> pointer as <i>lpForwardList</i>. If a <b>NULL</b> destination address is specified for an entry in the forwarding list, the operation acts as a do-not-disturb.

Forwarding status of an address can also be affected externally; for example, by administrative actions at the switch or by a user from another station. It may not be possible for the service provider to be aware of this state change, and it may not be able to keep in synchronization with the forwarding state known to the switch.

Because a service provider may not know the forwarding state of the address "for sure" (that is, it may have been forwarded or unforwarded in an unknown way), 
<b>lineForward</b> succeeds unless it fails to set the new forwarding instructions. In other words, a request that all forwarding be canceled at a time that there is no forwarding in effect is successful. This is because there is no "unforwarding"—you can only change the previous set of forwarding instructions.

The success or failure of this operation does not depend on the previous set of forwarding instructions, and the same is true when setting different forwarding instructions. The provider should "unforward everything" prior to setting the new forwarding instructions. Because this can take time in analog telephony environments, a provider may also want to compare the current forwarding with the new one, and only issue instructions to the switch to get to the final state (leaving unchanged forwarding unaffected).

Invoking 
<b>lineForward</b> when 
<a href="/windows/desktop/api/tapi/ns-tapi-lineforwardlist">LINEFORWARDLIST</a> has <i>dwNumEntries</i> set to zero has the same effect as providing a <b>NULL</b><i>lpForwardList</i> parameter. It cancels all forwarding currently in effect.





> [!NOTE]
> The tapi.h header defines lineForward as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/forward-ovr">Forward Overview</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineforwardlist">LINEFORWARDLIST</a>



<a href="/windows/desktop/Tapi/line-addressstate">LINE_ADDRESSSTATE</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
