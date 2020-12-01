---
UID: NF:tapi.phoneSetHookSwitch
title: phoneSetHookSwitch function (tapi.h)
description: The phoneSetHookSwitch function sets the hook state of the specified open phone's hookswitch devices to the specified mode. Only the hookswitch state of the hookswitch devices listed is affected.
helpviewer_keywords: ["_tapi2_phonesethookswitch","phoneSetHookSwitch","phoneSetHookSwitch function [TAPI 2.2]","tapi/phoneSetHookSwitch","tapi2.phonesethookswitch"]
old-location: tapi2\phonesethookswitch.htm
tech.root: tapi3
ms.assetid: 048f98e3-ac1b-47f8-85c8-97e7b7690030
ms.date: 12/05/2018
ms.keywords: _tapi2_phonesethookswitch, phoneSetHookSwitch, phoneSetHookSwitch function [TAPI 2.2], tapi/phoneSetHookSwitch, tapi2.phonesethookswitch
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
 - phoneSetHookSwitch
 - tapi/phoneSetHookSwitch
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
 - phoneSetHookSwitch
---

# phoneSetHookSwitch function


## -description

The 
<b>phoneSetHookSwitch</b> function sets the hook state of the specified open phone's hookswitch devices to the specified mode. Only the hookswitch state of the hookswitch devices listed is affected.

## -parameters

### -param hPhone

Handle to the open phone device. The application must be the owner of the phone.

### -param dwHookSwitchDevs

Device whose hookswitch mode is to be set. This parameter uses one and only one of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ Constants</a>. 







#### PHONEHOOKSWITCHDEV_HANDSET

The phone's handset.



#### PHONEHOOKSWITCHDEV_SPEAKER

The phone's speakerphone or adjunct.



#### PHONEHOOKSWITCHDEV_HEADSET

The phone's headset.

### -param dwHookSwitchMode

Hookswitch mode to set. This parameter uses one and only one of the 
<a href="/windows/desktop/Tapi/phonehookswitchmode--constants">PHONEHOOKSWITCHMODE_ Constants</a>. 







#### PHONEHOOKSWITCHMODE_ONHOOK

The device's microphone and speaker are both onhook.



#### PHONEHOOKSWITCHMODE_MIC

The device's microphone is active, the speaker is mute.



#### PHONEHOOKSWITCHMODE_SPEAKER

The device's speaker is active, the microphone is mute.



#### PHONEHOOKSWITCHMODE_MICSPEAKER

The device's microphone and speaker are both active.

## -returns

Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOTOWNER, PHONEERR_NOMEM, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALHOOKSWITCHMODE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_UNINITIALIZED.

## -remarks

The hookswitch mode is the same for all specified devices. If different settings are desired, this function can be invoked multiple times with a different set of parameters. A 
<a href="/windows/desktop/Tapi/phone-state">PHONE_STATE</a> message is sent to the application after the hookswitch state has changed.

## -see-also

<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a>



<a href="/windows/desktop/Tapi/phone-state">PHONE_STATE</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>