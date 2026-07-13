---
UID: NF:tapi.phoneGetIconA
title: phoneGetIconA function (tapi.h)
description: The phoneGetIcon function allows an application to retrieve a service phone device-specific (or provider-specific) icon that can be displayed to the user. (phoneGetIconA)
helpviewer_keywords: ["phoneGetIconA", "tapi/phoneGetIconA"]
old-location: tapi2\phonegeticon.htm
tech.root: tapi3
ms.assetid: 6c0fa053-387e-4c1f-a972-b7cd42a1ad00
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegeticon, phoneGetIcon, phoneGetIcon function [TAPI 2.2], phoneGetIconA, phoneGetIconW, tapi/phoneGetIcon, tapi/phoneGetIconA, tapi/phoneGetIconW, tapi2.phonegeticon
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: phoneGetIconW (Unicode) and phoneGetIconA (ANSI)
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
 - phoneGetIconA
 - tapi/phoneGetIconA
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
 - phoneGetIcon
 - phoneGetIconA
 - phoneGetIconW
---

# phoneGetIconA function


## -description

The 
<b>phoneGetIcon</b> function allows an application to retrieve a service phone device-specific (or provider-specific) icon that can be displayed to the user.

## -parameters

### -param dwDeviceID

Identifier of the phone device whose icon is requested.

### -param lpszDeviceClass

Pointer to a <b>null</b>-terminated string that identifies a device class name. This device class allows the application to select a specific sub-icon applicable to that device class. This parameter is optional and can be left <b>NULL</b> or empty, in which case the highest-level icon associated with the phone device rather than a specified media stream device would be selected.

### -param lphIcon

Pointer to a memory location in which the handle to the icon is returned.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_BADDEVICEID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_OPERATIONFAILED, PHONEERR_INVALDEVICECLASS, PHONEERR_UNINITIALIZED, PHONEERR_NOMEM, PHONEERR_NODEVICE.

## -remarks

The 
<b>phoneGetIcon</b> function causes the provider to return a handle (in <i>lphIcon</i>) to an icon resource (obtained from 
<a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>) associated with the specified phone. The icon handle is for a resource associated with the provider; the application must use 
<a href="/windows/desktop/api/winuser/nf-winuser-copyicon">CopyIcon</a> if it wants to reference the icon after the provider is unloaded, which is unlikely to happen as long as the application has the phone open.

The <i>lpszDeviceClass</i> parameter allows the provider to return different icons based on the type of service being referenced by the caller. The permitted strings are the same as for 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a>. For example, if the phone supports the Comm API, passing "COMM" as <i>lpszDeviceClass</i> causes the provider to return an icon related specifically to the Comm device functions of the service provider. The parameters "tapi/phone", "", or <b>NULL</b> can be used to request the icon for the phone service.

For applications using a TAPI version earlier than 2.0, if the provider does not return an icon (whether because the given device class is invalid or the provider does not support icons), TAPI substitutes a generic  Telephony phone device icon. For applications using TAPI version 2.0 or later, TAPI substitutes the default phone icon only if the <i>lpszDeviceClass</i> parameter is "tapi/phone", "", or <b>NULL</b>. For any other device class, if the given device class is not valid or the provider does not support icons for the class, 
<b>phoneGetIcon</b> returns PHONEERR_INVALDEVICECLASS.





> [!NOTE]
> The tapi.h header defines phoneGetIcon as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a>
