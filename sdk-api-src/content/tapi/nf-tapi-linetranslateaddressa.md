---
UID: NF:tapi.lineTranslateAddressA
title: lineTranslateAddressA function (tapi.h)
description: The lineTranslateAddress function translates the specified address into another format. (lineTranslateAddressA)
helpviewer_keywords: ["lineTranslateAddressA", "tapi/lineTranslateAddressA"]
old-location: tapi2\linetranslateaddress.htm
tech.root: tapi3
ms.assetid: 0347d526-9596-4b42-8075-07318bf39634
ms.date: 12/05/2018
ms.keywords: _tapi2_linetranslateaddress, lineTranslateAddress, lineTranslateAddress function [TAPI 2.2], lineTranslateAddressA, lineTranslateAddressW, tapi/lineTranslateAddress, tapi/lineTranslateAddressA, tapi/lineTranslateAddressW, tapi2.linetranslateaddress
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineTranslateAddressW (Unicode) and lineTranslateAddressA (ANSI)
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
 - lineTranslateAddressA
 - tapi/lineTranslateAddressA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
 - Ext-MS-Win-ras-tapi32-l1-1-0.dll
api_name:
 - lineTranslateAddress
 - lineTranslateAddressA
 - lineTranslateAddressW
---

# lineTranslateAddressA function


## -description

The 
<b>lineTranslateAddress</b> function translates the specified address into another format.

## -parameters

### -param hLineApp

Handle returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>. If a TAPI 2.x application has not yet called the 
<b>lineInitializeEx</b> function, it can set this parameter to <b>NULL</b>. TAPI 1.4 applications must still call 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitialize">lineInitialize</a> first.

### -param dwDeviceID

Device identifier of the line device upon which the call is to be dialed, so that variations in dialing procedures on different lines can be applied to the translation process.

### -param dwAPIVersion

Highest version of TAPI supported by the application (not necessarily the value negotiated by 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a> on some particular line device).

### -param lpszAddressIn

Pointer to a <b>null</b>-terminated string that contains the address of the information that is to be extracted for translation. Must be in either the canonical address format, or an arbitrary string of dialable digits (non-canonical). This parameter must not be <b>NULL</b>. If the <i>AddressIn</i> contains a subaddress or name field, or additional addresses separated from the first address by CR and LF characters, only the first address is translated.

### -param dwCard

Credit card to be used for dialing. This parameter is only valid if the CARDOVERRIDE bit is set in <i>dwTranslateOptions</i>. This parameter specifies the permanent identifier of a Card entry in the [Cards] section in the registry (as obtained from 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">lineTranslateCaps</a>) that should be used instead of the <b>PreferredCardID</b> specified in the definition of the <b>CurrentLocation</b>. It does not cause the <i>PreferredCardID</i> parameter of the current Location entry in the registry to be modified; the override applies only to the current translation operation. This parameter is ignored if the CARDOVERRIDE bit is not set in <i>dwTranslateOptions</i>.

### -param dwTranslateOptions

Associated operations to be performed prior to the translation of the address into a dialable string. This parameter uses one of the 
<a href="/windows/desktop/Tapi/linetranslateoption--constants">LINETRANSLATEOPTION_ Constants</a>. 




If you have set the LINETRANSLATEOPTION_CANCELCALLWAITING bit, it is also advisable to set the LINECALLPARAMFLAGS_SECURE bit in the <b>dwCallParamFlags</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a> structure (passed in to 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> through the <i>lpCallParams</i> parameter). This prevents the line device from using dialable digits to suppress call interrupts.

### -param lpTranslateOutput

Pointer to an application-allocated memory area to contain the output of the translation operation, of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslateoutput">LINETRANSLATEOUTPUT</a>. Prior to calling 
<b>lineTranslateAddress</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_INVALPOINTER, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_NODRIVER, LINEERR_INIFILECORRUPT, LINEERR_NOMEM, LINEERR_INVALADDRESS, LINEERR_OPERATIONFAILED, LINEERR_INVALAPPHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCARD, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALPARAM.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/win32/tapi/address-ovr#canonical-addresses">Canonical addresses</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linetranslateoutput">LINETRANSLATEOUTPUT</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/Tapi/tapi-version-negotiation">TAPI Version Negotiation</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>

## -remarks

> [!NOTE]
> The tapi.h header defines lineTranslateAddress as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
