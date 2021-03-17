---
UID: NF:tspi.TSPI_phoneGetLamp
title: TSPI_phoneGetLamp function (tspi.h)
description: The TSPI_phoneGetLamp function returns the current lamp mode of the specified lamp.
helpviewer_keywords: ["TSPI_phoneGetLamp","TSPI_phoneGetLamp function [TAPI 2.2]","_tspi_tspi_phonegetlamp","tspi.tspi_phonegetlamp","tspi/TSPI_phoneGetLamp"]
old-location: tspi\tspi_phonegetlamp.htm
tech.root: tapi3
ms.assetid: 121032ec-e9ec-4896-b114-3db2b3336812
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetLamp, TSPI_phoneGetLamp function [TAPI 2.2], _tspi_tspi_phonegetlamp, tspi.tspi_phonegetlamp, tspi/TSPI_phoneGetLamp
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
 - TSPI_phoneGetLamp
 - tspi/TSPI_phoneGetLamp
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
 - TSPI_phoneGetLamp
---

# TSPI_phoneGetLamp function


## -description

The 
<b>TSPI_phoneGetLamp</b> function returns the current lamp mode of the specified lamp.

## -parameters

### -param hdPhone

The handle to the phone whose lamp mode is to be retrieved.

### -param dwButtonLampID

The identifier of the lamp to be queried.

### -param lpdwLampMode

A pointer to a memory location into which the service provider writes the lamp mode status of the given lamp. This parameter can have at most one of the 
<a href="/windows/desktop/Tapi/phonelampmode--constants">PHONELAMPMODE_ constants</a>.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALBUTTONLAMPID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.

## -remarks

Phone sets that have multiple lamps per button should be modeled using multiple button/lamps pairs. Each additional button/lamp pair should use a DUMMY button.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/Tapi/phonelampmode--constants">PHONELAMPMODE_ Constants</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonesetlamp">TSPI_phoneSetLamp</a>