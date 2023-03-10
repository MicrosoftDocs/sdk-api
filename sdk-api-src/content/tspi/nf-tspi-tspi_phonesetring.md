---
UID: NF:tspi.TSPI_phoneSetRing
title: TSPI_phoneSetRing function (tspi.h)
description: The TSPI_phoneSetRing function rings the specified open phone device using the specified ring mode and volume.
helpviewer_keywords: ["TSPI_phoneSetRing","TSPI_phoneSetRing function [TAPI 2.2]","_tspi_tspi_phonesetring","tspi.tspi_phonesetring","tspi/TSPI_phoneSetRing"]
old-location: tspi\tspi_phonesetring.htm
tech.root: tapi3
ms.assetid: 8540f39e-4891-48d9-a5b0-b928eeb4be0d
ms.date: 12/05/2018
ms.keywords: TSPI_phoneSetRing, TSPI_phoneSetRing function [TAPI 2.2], _tspi_tspi_phonesetring, tspi.tspi_phonesetring, tspi/TSPI_phoneSetRing
req.header: tspi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_phoneSetRing
 - tspi/TSPI_phoneSetRing
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneSetRing
---

# TSPI_phoneSetRing function


## -description

The 
<b>TSPI_phoneSetRing</b> function rings the specified open phone device using the specified ring mode and volume.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdPhone

The handle to the phone to be rung.

### -param dwRingMode

The ringing pattern with which to ring the phone. This parameter must be within the range from zero through the value of the <b>dwNumRingModes</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure. If <b>dwNumRingModes</b> is zero, the ring mode of the phone cannot be controlled; if <b>dwNumRingModes</b> is 1, a value of 0 for <i>dwRingMode</i> indicates that the phone should not be rung (silence), and other values from 1 through <b>dwNumRingModes</b> are valid ring modes for the phone device.

### -param dwVolume

The volume level with which the phone is to be rung. This is a number in the range from 0x00000000 (silence) through 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service-provider specific. A value for <i>dwVolume</i> that is out of range is clamped by TAPI to the nearest value in range.

## -returns

Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALRINGMODE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.

## -remarks

The service provider defines the actual audible ringing patterns corresponding to each of the phone's ring modes.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetring">TSPI_phoneGetRing</a>