---
UID: NF:tapi.lineTranslateDialogA
title: lineTranslateDialogA function (tapi.h)
description: The lineTranslateDialog function displays an application-modal dialog box that allows the user to change the current location of a phone number about to be dialed, adjust location and calling card parameters, and see the effect. (lineTranslateDialogA)
helpviewer_keywords: ["lineTranslateDialogA", "tapi/lineTranslateDialogA"]
old-location: tapi2\linetranslatedialog.htm
tech.root: tapi3
ms.assetid: c9fd7abb-3b4b-442b-badc-371a12724f67
ms.date: 12/05/2018
ms.keywords: _tapi2_linetranslatedialog, lineTranslateDialog, lineTranslateDialog function [TAPI 2.2], lineTranslateDialogA, lineTranslateDialogW, tapi/lineTranslateDialog, tapi/lineTranslateDialogA, tapi/lineTranslateDialogW, tapi2.linetranslatedialog
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineTranslateDialogW (Unicode) and lineTranslateDialogA (ANSI)
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
 - lineTranslateDialogA
 - tapi/lineTranslateDialogA
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
 - lineTranslateDialog
 - lineTranslateDialogA
 - lineTranslateDialogW
---

# lineTranslateDialogA function


## -description

The 
<b>lineTranslateDialog</b> function displays an application-modal dialog box that allows the user to change the current location of a phone number about to be dialed, adjust location and calling card parameters, and see the effect.

## -parameters

### -param hLineApp

Application handle returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>. If an application has not yet called the 
<b>lineInitializeEx</b> function, it can set the <i>hLineApp</i> parameter to zero.

### -param dwDeviceID

Device identifier for the line device upon which the call is intended to be dialed, so that variations in dialing procedures on different lines can be applied to the translation process.

### -param dwAPIVersion

Highest version of TAPI supported by the application (not necessarily the value negotiated by 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a> on the line device indicated by <i>dwDeviceID</i>).

### -param hwndOwner

Handle to a window to which the dialog box is to be attached. Can be a <b>NULL</b> value to indicate that any window created during the function should have no owner window.

### -param lpszAddressIn

Pointer to a <b>null</b>-terminated string containing a phone number that is used, in the lower portion of the dialog box, to show the effect of the user's changes on the location parameters. The number must be in canonical format; if noncanonical, the phone number portion of the dialog box is not displayed. This pointer can be left <b>NULL</b>, in which case the phone number portion of the dialog box is not displayed. If the <i>lpszAddressIn</i> parameter contains a subaddress or name field, or additional addresses separated from the first address by CR and LF characters, only the first address is used in the dialog box.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_INVALPARAM, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_INVALPOINTER, LINEERR_INIFILECORRUPT, LINEERR_NODRIVER, LINEERR_INUSE, LINEERR_NOMEM, LINEERR_INVALADDRESS, LINEERR_INVALAPPHANDLE, LINEERR_OPERATIONFAILED.

## -remarks

In TAPI version 2.0 or later, it is possible for multiple instances of this dialog box to be opened. In TAPI versions earlier than 2.0, LINEERR_INUSE is returned if the dialog box is already displayed by another application (it cannot be open more than once). In these versions, TAPI brings the existing dialog box to the front, and the error indicates that any particulars related to the address passed in by the current application have not been handled, because that address was not processed by the function.

The application must call 
<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a> after this function to obtain any changes the user made to the telephony address translation parameters, and call 
<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a> to obtain a dialable string based on the user's new selections.

If any function related to address translation (for example, 
<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a> or 
<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a>) returns LINEERR_INIFILECORRUPT, the application should call 
<b>lineTranslateDialog</b>. The 
<b>lineTranslateDialog</b> function detects the errors and corrects them, and reports the action taken to the user.





> [!NOTE]
> The tapi.h header defines lineTranslateDialog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a>
