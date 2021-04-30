---
UID: NF:tspi.TSPI_phoneSetVolume
title: TSPI_phoneSetVolume function (tspi.h)
description: The TSPI_phoneSetVolume function sets the volume of the speaker component of the specified hookswitch device to the specified level.
helpviewer_keywords: ["TSPI_phoneSetVolume","TSPI_phoneSetVolume function [TAPI 2.2]","_tspi_tspi_phonesetvolume","tspi.tspi_phonesetvolume","tspi/TSPI_phoneSetVolume"]
old-location: tspi\tspi_phonesetvolume.htm
tech.root: tapi3
ms.assetid: c9aa2a3a-71ef-4214-b165-00a9620bb7e9
ms.date: 12/05/2018
ms.keywords: TSPI_phoneSetVolume, TSPI_phoneSetVolume function [TAPI 2.2], _tspi_tspi_phonesetvolume, tspi.tspi_phonesetvolume, tspi/TSPI_phoneSetVolume
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
 - TSPI_phoneSetVolume
 - tspi/TSPI_phoneSetVolume
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
 - TSPI_phoneSetVolume
---

# TSPI_phoneSetVolume function


## -description

The 
<b>TSPI_phoneSetVolume</b> function sets the volume of the speaker component of the specified hookswitch device to the specified level.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdPhone

The handle to the phone containing the speaker whose volume is to be set.

### -param dwHookSwitchDev

Identifies the hookswitch device whose speaker's volume is to be set. This parameter uses one of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ constants</a>.

### -param dwVolume

A <b>DWORD</b> specifying the new volume level of the hookswitch device. This is a number in the range from 0x00000000 (silence) through 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service-provider specific. A value for <i>dwVolume</i> that is out of range is clamped by TAPI to the nearest value in range.

## -returns

Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.

## -remarks

None.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ Constants</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>