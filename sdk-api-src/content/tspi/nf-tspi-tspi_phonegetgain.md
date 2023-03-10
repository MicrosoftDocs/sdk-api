---
UID: NF:tspi.TSPI_phoneGetGain
title: TSPI_phoneGetGain function (tspi.h)
description: The TSPI_phoneGetGain function returns the gain setting of the microphone of the specified phone's hookswitch device.
helpviewer_keywords: ["TSPI_phoneGetGain","TSPI_phoneGetGain function [TAPI 2.2]","_tspi_tspi_phonegetgain","tspi.tspi_phonegetgain","tspi/TSPI_phoneGetGain"]
old-location: tspi\tspi_phonegetgain.htm
tech.root: tapi3
ms.assetid: 2efe9d36-3179-486b-9691-78a88452d91c
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetGain, TSPI_phoneGetGain function [TAPI 2.2], _tspi_tspi_phonegetgain, tspi.tspi_phonegetgain, tspi/TSPI_phoneGetGain
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
 - TSPI_phoneGetGain
 - tspi/TSPI_phoneGetGain
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
 - TSPI_phoneGetGain
---

# TSPI_phoneGetGain function


## -description

The 
<b>TSPI_phoneGetGain</b> function returns the gain setting of the microphone of the specified phone's hookswitch device.

## -parameters

### -param hdPhone

The handle to the phone whose gain is to be retrieved.

### -param dwHookSwitchDev

The hookswitch device whose gain level is queried. This parameter may be one and only one of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ Constants</a>.

### -param lpdwGain

A pointer to a <b>DWORD</b>-sized location into which the service provider writes the current gain setting of the hookswitch microphone component. The <i>dwGain</i> gain parameter specifies the volume level of the hookswitch device. This is a number in the range from 0x00000000 (silence) through 0x0000FFFF (maximum volume). The actual granularity and quantization of gain settings in this range are service provider-specific.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonesetgain">TSPI_phoneSetGain</a>