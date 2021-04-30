---
UID: NF:tspi.TSPI_phoneGetVolume
title: TSPI_phoneGetVolume function (tspi.h)
description: The TSPI_phoneGetVolume function returns the volume setting of the specified phone's hookswitch device.
helpviewer_keywords: ["TSPI_phoneGetVolume","TSPI_phoneGetVolume function [TAPI 2.2]","_tspi_tspi_phonegetvolume","tspi.tspi_phonegetvolume","tspi/TSPI_phoneGetVolume"]
old-location: tspi\tspi_phonegetvolume.htm
tech.root: tapi3
ms.assetid: 4ea36cce-da68-47a3-ad79-4fc304a49451
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetVolume, TSPI_phoneGetVolume function [TAPI 2.2], _tspi_tspi_phonegetvolume, tspi.tspi_phonegetvolume, tspi/TSPI_phoneGetVolume
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
 - TSPI_phoneGetVolume
 - tspi/TSPI_phoneGetVolume
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
 - TSPI_phoneGetVolume
---

# TSPI_phoneGetVolume function


## -description

The 
<b>TSPI_phoneGetVolume</b> function returns the volume setting of the specified phone's hookswitch device.

## -parameters

### -param hdPhone

The handle to the phone containing the hookswitch device whose volume setting is to be retrieved.

### -param dwHookSwitchDev

Identifies a single hookswitch device whose volume level is queried. This parameter uses one of the 
<a href="/windows/desktop/Tapi/phonehookswitchdev--constants">PHONEHOOKSWITCHDEV_ constants</a>.

### -param lpdwVolume

A pointer to a <b>DWORD</b>-sized location into which the service provider writes the current volume setting of the hookswitch device. This is a number in the range from 0x00000000 (silence) through 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service-provider specific.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonesetvolume">TSPI_phoneSetVolume</a>