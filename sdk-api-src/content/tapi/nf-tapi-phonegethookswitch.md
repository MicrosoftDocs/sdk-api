---
UID: NF:tapi.phoneGetHookSwitch
title: phoneGetHookSwitch function (tapi.h)
description: The phoneGetHookSwitch function returns the current hookswitch mode of the specified open phone device.
helpviewer_keywords: ["_tapi2_phonegethookswitch","phoneGetHookSwitch","phoneGetHookSwitch function [TAPI 2.2]","tapi/phoneGetHookSwitch","tapi2.phonegethookswitch"]
old-location: tapi2\phonegethookswitch.htm
tech.root: tapi3
ms.assetid: 246f8b2b-8748-453d-b2b6-16771c0aad36
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegethookswitch, phoneGetHookSwitch, phoneGetHookSwitch function [TAPI 2.2], tapi/phoneGetHookSwitch, tapi2.phonegethookswitch
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - phoneGetHookSwitch
 - tapi/phoneGetHookSwitch
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
 - phoneGetHookSwitch
---

# phoneGetHookSwitch function


## -description

The 
<b>phoneGetHookSwitch</b> function returns the current hookswitch mode of the specified open phone device.

## -parameters

### -param hPhone

Handle to the open phone device.

### -param lpdwHookSwitchDevs

Pointer to a <b>DWORD</b> to be filled with the mode of the phone's hookswitch devices. If a bit position is <b>FALSE</b>, the corresponding hookswitch device is onhook; if <b>TRUE</b>, the microphone and/or speaker part of the corresponding hookswitch device is offhook. To find out whether the microphone and/or speaker are enabled, the application can use 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetstatus">phoneGetStatus</a>. This parameter uses one or more of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ Constants</a>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED.

## -remarks

After the hookswitch state of a device changes, and if hookswitch monitoring is enabled, the application is sent a 
<a href="/windows/desktop/Tapi/phone-state">PHONE_STATE</a> message.

## -see-also

<a href="/windows/desktop/Tapi/phone-state">PHONE_STATE</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetstatus">phoneGetStatus</a>