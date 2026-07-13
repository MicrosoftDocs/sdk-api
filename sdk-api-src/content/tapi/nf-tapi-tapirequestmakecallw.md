---
UID: NF:tapi.tapiRequestMakeCallW
title: tapiRequestMakeCallW function (tapi.h)
description: The tapiRequestMakeCallW (Unicode) function (tapi.h) requests the establishment of a voice call. 
helpviewer_keywords: ["_tapi2_tapirequestmakecall", "tapi/tapiRequestMakeCall", "tapi/tapiRequestMakeCallW", "tapi2.tapirequestmakecall", "tapiRequestMakeCall", "tapiRequestMakeCall function [TAPI 2.2]", "tapiRequestMakeCallW"]
old-location: tapi2\tapirequestmakecall.htm
tech.root: tapi3
ms.assetid: bdbc1565-6570-4fad-890c-fb3965cce452
ms.date: 08/09/2022
ms.keywords: _tapi2_tapirequestmakecall, tapi/tapiRequestMakeCall, tapi/tapiRequestMakeCallA, tapi/tapiRequestMakeCallW, tapi2.tapirequestmakecall, tapiRequestMakeCall, tapiRequestMakeCall function [TAPI 2.2], tapiRequestMakeCallA, tapiRequestMakeCallW
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: tapiRequestMakeCallW (Unicode) and tapiRequestMakeCallA (ANSI)
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
 - tapiRequestMakeCallW
 - tapi/tapiRequestMakeCallW
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
 - tapiRequestMakeCall
 - tapiRequestMakeCallA
 - tapiRequestMakeCallW
---

# tapiRequestMakeCallW function


## -description

The <b>tapiRequestMakeCall</b> function requests the establishment of a voice call. A call-manager application is responsible for establishing the call on behalf of the requesting application, which is then controlled by the user's call-manager application.

## -parameters

### -param lpszDestAddress

Pointer to a memory location where the <b>null</b>-terminated destination address of the call request is located. The address can use the 
[canonical address](/windows/win32/tapi/address-ovr#canonical-addresses) format. Validity of the specified address is not checked by this operation. The maximum length of the address is TAPIMAXDESTADDRESSSIZE characters, which includes the <b>NULL</b> terminator.

### -param lpszAppName

Pointer to a memory location where the <b>null</b>-terminated user-friendly application name of the call request is located. This pointer can be left <b>NULL</b> if the application does not supply an application name. The maximum length of the address is TAPIMAXAPPNAMESIZE characters, which includes the <b>NULL</b> terminator. Longer strings are truncated.

### -param lpszCalledParty

Pointer to a memory location where the <b>null</b>-terminated called party name for the called party of the call is located. This pointer can be left <b>NULL</b> if the application does not wish to supply this information. The maximum length of the string is TAPIMAXCALLEDPARTYSIZE characters, which includes the <b>NULL</b> terminator. Longer strings are truncated.

### -param lpszComment

Pointer to a memory location where the <b>null</b>-terminated comment about the call is located. This pointer can be left <b>NULL</b> if the application does not supply a comment. The maximum length of the address is TAPIMAXCOMMENTSIZE characters, which includes the <b>NULL</b> terminator. Longer strings are truncated.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible error return value are:

TAPIERR_NOREQUESTRECIPIENT, TAPIERR_INVALDESTADDRESS, TAPIERR_REQUESTQUEUEFULL, TAPIERR_INVALPOINTER.

## -remarks

A telephony-enabled application can request that a call be placed on its behalf by invoking 
<b>tapiRequestMakeCall</b>, providing only the destination address for the call. This request is forwarded to the user's call-control application, which places the call on behalf of the original application. A default call-control application is provided as part of  Telephony. Users can replace this with a call-control application of their choice.

Invoking 
<b>tapiRequestMakeCall</b> when no call control application is running returns the TAPIERR_NOREQUESTRECIPIENT error indication. If the call control application is not running, TAPI attempts to launch the highest-priority call control application (which is listed for <b>RequestMakeCall</b> in the registry). Invoking this function when the Assisted TAPI request queue is full returns the TAPIERR_REQUESTQUEUEFULL error.





> [!NOTE]
> The tapi.h header defines tapiRequestMakeCall as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/assisted-telephony-services-reference">Assisted Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
