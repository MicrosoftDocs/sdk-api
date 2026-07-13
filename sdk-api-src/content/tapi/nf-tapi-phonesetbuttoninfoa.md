---
UID: NF:tapi.phoneSetButtonInfoA
title: phoneSetButtonInfoA function (tapi.h)
description: The phoneSetButtonInfo function sets information about the specified button on the specified phone. (phoneSetButtonInfoA)
helpviewer_keywords: ["phoneSetButtonInfoA", "tapi/phoneSetButtonInfoA"]
old-location: tapi2\phonesetbuttoninfo.htm
tech.root: tapi3
ms.assetid: f51581a9-7b2a-4ba0-83fa-f464c8202648
ms.date: 12/05/2018
ms.keywords: _tapi2_phonesetbuttoninfo, phoneSetButtonInfo, phoneSetButtonInfo function [TAPI 2.2], phoneSetButtonInfoA, phoneSetButtonInfoW, tapi/phoneSetButtonInfo, tapi/phoneSetButtonInfoA, tapi/phoneSetButtonInfoW, tapi2.phonesetbuttoninfo
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: phoneSetButtonInfoW (Unicode) and phoneSetButtonInfoA (ANSI)
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
 - phoneSetButtonInfoA
 - tapi/phoneSetButtonInfoA
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
 - phoneSetButtonInfo
 - phoneSetButtonInfoA
 - phoneSetButtonInfoW
---

# phoneSetButtonInfoA function


## -description

The 
<b>phoneSetButtonInfo</b> function sets information about the specified button on the specified phone.

## -parameters

### -param hPhone

Handle to the open phone device. The application must be the owner of the phone device.

### -param dwButtonLampID

Button on the phone device.

### -param lpButtonInfo

Pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo">PHONEBUTTONINFO</a>. This data structure describes the mode, the function, and provides additional descriptive text about the button.

## -returns

Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALBUTTONLAMPID, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONEHANDLE, PHONEERR_STRUCTURETOOSMALL, PHONEERR_INVALPOINTER, PHONEERR_UNINITIALIZED, PHONEERR_NOTOWNER, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL, PHONEERR_RESOURCEUNAVAIL.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo">PHONEBUTTONINFO</a>



<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>

## -remarks

> [!NOTE]
> The tapi.h header defines phoneSetButtonInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
