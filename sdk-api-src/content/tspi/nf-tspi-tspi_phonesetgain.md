---
UID: NF:tspi.TSPI_phoneSetGain
title: TSPI_phoneSetGain function (tspi.h)
description: The TSPI_phoneSetGain function sets the gain of the microphone of the specified hookswitch device to the specified gain level.
helpviewer_keywords: ["TSPI_phoneSetGain","TSPI_phoneSetGain function [TAPI 2.2]","_tspi_tspi_phonesetgain","tspi.tspi_phonesetgain","tspi/TSPI_phoneSetGain"]
old-location: tspi\tspi_phonesetgain.htm
tech.root: tapi3
ms.assetid: c7eb459d-6b59-4bc1-8f2b-c3c03a0a5bd9
ms.date: 12/05/2018
ms.keywords: TSPI_phoneSetGain, TSPI_phoneSetGain function [TAPI 2.2], _tspi_tspi_phonesetgain, tspi.tspi_phonesetgain, tspi/TSPI_phoneSetGain
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
 - TSPI_phoneSetGain
 - tspi/TSPI_phoneSetGain
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
 - TSPI_phoneSetGain
---

# TSPI_phoneSetGain function


## -description

The 
<b>TSPI_phoneSetGain</b> function sets the gain of the microphone of the specified hookswitch device to the specified gain level.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdPhone

The handle to the phone containing the hookswitch device whose gain is to be set.

### -param dwHookSwitchDev

The hookswitch device whose microphone's gain is to be set. This parameter uses one and only one of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ Constants</a>.

### -param dwGain

A <b>DWORD</b>-sized location containing the desired new gain setting of the device. This is a number in the range from 0x00000000 (silence) through 0x0000FFFF (maximum volume). The actual granularity and quantization of gain settings in this range are service-provider-specific. A value for <i>dwGain</i> that is out of range is clamped by TAPI to the nearest in-range value.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>