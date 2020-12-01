---
UID: NF:tspi.TSPI_phoneGetRing
title: TSPI_phoneGetRing function (tspi.h)
description: The TSPI_phoneGetRing function enables an application to query the specified open phone device as to its current ring mode.
helpviewer_keywords: ["TSPI_phoneGetRing","TSPI_phoneGetRing function [TAPI 2.2]","_tspi_tspi_phonegetring","tspi.tspi_phonegetring","tspi/TSPI_phoneGetRing"]
old-location: tspi\tspi_phonegetring.htm
tech.root: tapi3
ms.assetid: dcdfff60-e853-4ad7-a2b4-ddfc0ee73a48
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetRing, TSPI_phoneGetRing function [TAPI 2.2], _tspi_tspi_phonegetring, tspi.tspi_phonegetring, tspi/TSPI_phoneGetRing
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
 - TSPI_phoneGetRing
 - tspi/TSPI_phoneGetRing
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
 - TSPI_phoneGetRing
---

# TSPI_phoneGetRing function


## -description

The 
<b>TSPI_phoneGetRing</b> function enables an application to query the specified open phone device as to its current ring mode.

## -parameters

### -param hdPhone

The handle to the phone whose ring mode is to be queried.

### -param lpdwRingMode

The ringing pattern with which the phone is ringing. Zero indicates that the phone is not ringing.

### -param lpdwVolume

The volume level with which the phone is ringing. This is a number in the range from 0x00000000 (silence) through 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service-provider specific.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL.

## -remarks

The service provider defines the actual audible ringing patterns corresponding to each of phone's ring modes.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonesetring">TSPI_phoneSetRing</a>