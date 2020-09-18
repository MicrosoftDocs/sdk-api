---
UID: NF:tapi.phoneSetVolume
title: phoneSetVolume function (tapi.h)
description: The phoneSetVolume function sets the volume of the speaker component of the specified hookswitch device to the specified level.
helpviewer_keywords: ["_tapi2_phonesetvolume","phoneSetVolume","phoneSetVolume function [TAPI 2.2]","tapi/phoneSetVolume","tapi2.phonesetvolume"]
old-location: tapi2\phonesetvolume.htm
tech.root: tapi3
ms.assetid: 114aba48-f058-47c9-9ee7-493bd758b8a6
ms.date: 12/05/2018
ms.keywords: _tapi2_phonesetvolume, phoneSetVolume, phoneSetVolume function [TAPI 2.2], tapi/phoneSetVolume, tapi2.phonesetvolume
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
 - phoneSetVolume
 - tapi/phoneSetVolume
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
 - phoneSetVolume
---

# phoneSetVolume function


## -description

The 
<b>phoneSetVolume</b> function sets the volume of the speaker component of the specified hookswitch device to the specified level.

## -parameters

### -param hPhone

Handle to the open phone device. The application must be the owner of the phone.

### -param dwHookSwitchDev

Hookswitch device whose speaker's volume is to be set, one of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ Constants</a>.

### -param dwVolume

New volume setting of the device. The <i>dwVolume</i> parameter specifies the volume level of the hookswitch device. This is a number in the range 0x00000000 (silence) to 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service provider-specific. A value for <i>dwVolume</i> that is out of range is set to the nearest value in the range.

## -returns

Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_NOTOWNER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.

## -see-also

<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>