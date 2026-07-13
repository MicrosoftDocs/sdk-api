---
UID: NF:tapi.lineSetTollListW
title: lineSetTollListW function (tapi.h)
description: The lineSetTollListW (Unicode) function (tapi.h) manipulates the toll list.
helpviewer_keywords: ["_tapi2_linesettolllist", "lineSetTollList", "lineSetTollList function [TAPI 2.2]", "lineSetTollListW", "tapi/lineSetTollList", "tapi/lineSetTollListW", "tapi2.linesettolllist"]
old-location: tapi2\linesettolllist.htm
tech.root: tapi3
ms.assetid: 40471e45-cb1d-4730-ba35-ffec99953235
ms.date: 08/09/2022
ms.keywords: _tapi2_linesettolllist, lineSetTollList, lineSetTollList function [TAPI 2.2], lineSetTollListA, lineSetTollListW, tapi/lineSetTollList, tapi/lineSetTollListA, tapi/lineSetTollListW, tapi2.linesettolllist
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineSetTollListW (Unicode) and lineSetTollListA (ANSI)
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
 - lineSetTollListW
 - tapi/lineSetTollListW
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
 - lineSetTollList
 - lineSetTollListA
 - lineSetTollListW
---

# lineSetTollListW function


## -description

The 
<b>lineSetTollList</b> function manipulates the toll list.

## -parameters

### -param hLineApp

Application handle returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>. If an application has not yet called the 
<b>lineInitializeEx</b> function, it can set the <i>hLineApp</i> parameter to zero.

### -param dwDeviceID

Device identifier for the line device upon which the call is intended to be dialed, so that variations in dialing procedures on different lines can be applied to the translation process.

### -param lpszAddressInW

Pointer to a <b>null</b>-terminated string containing the address from which the prefix information is to be extracted for processing. This parameter must not be <b>NULL</b>, and it must be in the canonical address format.

### -param dwTollListOption

Toll list operation to be performed. This parameter uses one and only one of the 
<a href="/windows/desktop/Tapi/linetolllistoption--constants">LINETOLLLISTOPTION_ Constants</a>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NODRIVER, LINEERR_INVALAPPHANDLE, LINEERR_NOMEM, LINEERR_INVALADDRESS, LINEERR_OPERATIONFAILED, LINEERR_INVALPARAM, LINEERR_RESOURCEUNAVAIL, LINEERR_INIFILECORRUPT, LINEERR_UNINITIALIZED, LINEERR_INVALLOCATION.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>

## -remarks

> [!NOTE]
> The tapi.h header defines lineSetTollList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
