---
UID: NF:tapi.phoneGetVolume
title: phoneGetVolume function (tapi.h)
description: The phoneGetVolume function returns the volume setting of the specified phone's hookswitch device.
helpviewer_keywords: ["_tapi2_phonegetvolume","phoneGetVolume","phoneGetVolume function [TAPI 2.2]","tapi/phoneGetVolume","tapi2.phonegetvolume"]
old-location: tapi2\phonegetvolume.htm
tech.root: tapi3
ms.assetid: 049da2d5-4c31-4311-8dac-30545f8bf39b
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegetvolume, phoneGetVolume, phoneGetVolume function [TAPI 2.2], tapi/phoneGetVolume, tapi2.phonegetvolume
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
 - phoneGetVolume
 - tapi/phoneGetVolume
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
 - phoneGetVolume
---

# phoneGetVolume function


## -description

The 
<b>phoneGetVolume</b> function returns the volume setting of the specified phone's hookswitch device.

## -parameters

### -param hPhone

Handle to the open phone device.

### -param dwHookSwitchDev

A single hookswitch device whose volume level is queried. This parameter uses one of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ Constants</a>.

### -param lpdwVolume

Pointer to a <b>DWORD</b>. The function returns the current volume setting of the hookswitch device in this location. This is a number in the range 0x00000000 (silence) to 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service provider-specific.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPHONESTATE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.

## -see-also

<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>