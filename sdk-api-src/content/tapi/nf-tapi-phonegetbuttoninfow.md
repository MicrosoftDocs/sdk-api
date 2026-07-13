---
UID: NF:tapi.phoneGetButtonInfoW
title: phoneGetButtonInfoW function (tapi.h)
description: The phoneGetButtonInfoW (Unicode) function (tapi.h) returns information about the specified button.
helpviewer_keywords: ["_tapi2_phonegetbuttoninfo", "phoneGetButtonInfo", "phoneGetButtonInfo function [TAPI 2.2]", "phoneGetButtonInfoW", "tapi/phoneGetButtonInfo", "tapi/phoneGetButtonInfoW", "tapi2.phonegetbuttoninfo"]
old-location: tapi2\phonegetbuttoninfo.htm
tech.root: tapi3
ms.assetid: a4df5ba0-7fce-4d29-80a6-4f8f58ae1a83
ms.date: 08/09/2022
ms.keywords: _tapi2_phonegetbuttoninfo, phoneGetButtonInfo, phoneGetButtonInfo function [TAPI 2.2], phoneGetButtonInfoA, phoneGetButtonInfoW, tapi/phoneGetButtonInfo, tapi/phoneGetButtonInfoA, tapi/phoneGetButtonInfoW, tapi2.phonegetbuttoninfo
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: phoneGetButtonInfoW (Unicode) and phoneGetButtonInfoA (ANSI)
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
 - phoneGetButtonInfoW
 - tapi/phoneGetButtonInfoW
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
 - phoneGetButtonInfo
 - phoneGetButtonInfoA
 - phoneGetButtonInfoW
---

# phoneGetButtonInfoW function


## -description

The 
<b>phoneGetButtonInfo</b> function returns information about the specified button.

## -parameters

### -param hPhone

Handle to the open phone device.

### -param dwButtonLampID

Button on the phone device.

### -param lpButtonInfo

Pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo">PHONEBUTTONINFO</a>. This data structure describes the mode and the function, and provides additional descriptive text corresponding to the button.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALBUTTONLAMPID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_STRUCTURETOOSMALL, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo">PHONEBUTTONINFO</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>

## -remarks

> [!NOTE]
> The tapi.h header defines phoneGetButtonInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
