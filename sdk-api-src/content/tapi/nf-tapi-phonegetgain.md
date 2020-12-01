---
UID: NF:tapi.phoneGetGain
title: phoneGetGain function (tapi.h)
description: The phoneGetGain function returns the gain setting of the microphone of the specified phone's hookswitch device.
helpviewer_keywords: ["_tapi2_phonegetgain","phoneGetGain","phoneGetGain function [TAPI 2.2]","tapi/phoneGetGain","tapi2.phonegetgain"]
old-location: tapi2\phonegetgain.htm
tech.root: tapi3
ms.assetid: ea6ba2f0-ff79-41b8-9165-bb250077b2dc
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegetgain, phoneGetGain, phoneGetGain function [TAPI 2.2], tapi/phoneGetGain, tapi2.phonegetgain
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
 - phoneGetGain
 - tapi/phoneGetGain
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
 - phoneGetGain
---

# phoneGetGain function


## -description

The 
<b>phoneGetGain</b> function returns the gain setting of the microphone of the specified phone's hookswitch device.

## -parameters

### -param hPhone

Handle to the open phone device.

### -param dwHookSwitchDev

Hookswitch device whose gain level is queried. The <i>dwHookSwitchDev</i> parameter can have only one bit set. This parameter uses one and only one of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ Constants</a>.

### -param lpdwGain

Pointer to a <b>DWORD</b> containing the current gain setting of the hookswitch microphone component. The <i>dwGain</i> parameter specifies the volume level of the hookswitch device. This is a number in the range 0x00000000 (silence) to 0x0000FFFF (maximum volume). The actual granularity and quantization of gain settings in this range are service provider-specific.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.

## -see-also

<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>