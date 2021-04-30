---
UID: NF:tapi.phoneGetRing
title: phoneGetRing function (tapi.h)
description: The phoneGetRing function enables an application to query the specified open phone device as to its current ring mode.
helpviewer_keywords: ["_tapi2_phonegetring","phoneGetRing","phoneGetRing function [TAPI 2.2]","tapi/phoneGetRing","tapi2.phonegetring"]
old-location: tapi2\phonegetring.htm
tech.root: tapi3
ms.assetid: 7ce96ce5-ab7c-42cf-8d06-e50e676ddbd2
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegetring, phoneGetRing, phoneGetRing function [TAPI 2.2], tapi/phoneGetRing, tapi2.phonegetring
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
 - phoneGetRing
 - tapi/phoneGetRing
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
 - phoneGetRing
---

# phoneGetRing function


## -description

The 
<b>phoneGetRing</b> function enables an application to query the specified open phone device as to its current ring mode.

## -parameters

### -param hPhone

Handle to the open phone device.

### -param lpdwRingMode

Ringing pattern with which the phone is ringing. Zero indicates that the phone is not ringing.

### -param lpdwVolume

Volume level with which the phone is ringing. This is a number in the range 0x00000000 (silence) to 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service provider-specific.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPHONESTATE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_OPERATIONFAILED, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED.

## -remarks

The service provider defines the actual audible ringing patterns corresponding to each of the phone's ring modes.

## -see-also

<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>