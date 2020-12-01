---
UID: NF:tspi.TSPI_phoneSetLamp
title: TSPI_phoneSetLamp function (tspi.h)
description: The TSPI_phoneSetLamp function causes the specified lamp to be set on the specified open phone device in the specified lamp mode.
helpviewer_keywords: ["TSPI_phoneSetLamp","TSPI_phoneSetLamp function [TAPI 2.2]","_tspi_tspi_phonesetlamp","tspi.tspi_phonesetlamp","tspi/TSPI_phoneSetLamp"]
old-location: tspi\tspi_phonesetlamp.htm
tech.root: tapi3
ms.assetid: d525b5d2-f5f8-490b-9db8-06881060efe5
ms.date: 12/05/2018
ms.keywords: TSPI_phoneSetLamp, TSPI_phoneSetLamp function [TAPI 2.2], _tspi_tspi_phonesetlamp, tspi.tspi_phonesetlamp, tspi/TSPI_phoneSetLamp
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
 - TSPI_phoneSetLamp
 - tspi/TSPI_phoneSetLamp
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
 - TSPI_phoneSetLamp
---

# TSPI_phoneSetLamp function


## -description

The 
<b>TSPI_phoneSetLamp</b> function causes the specified lamp to be set on the specified open phone device in the specified lamp mode.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdPhone

The handle to the phone whose lamp is to be set.

### -param dwButtonLampID

The button whose lamp is to be set.

### -param dwLampMode

Specifies how the lamp is to be lit. The <i>dwLampMode</i> parameter can only have one of the 
<a href="/windows/desktop/Tapi/phonelampmode--constants">PHONELAMPMODE_ constants</a>.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALBUTTONLAMPID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALLAMPMODE, PHONEERR_OPERATIONUNAVAIL.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/Tapi/phonelampmode--constants">PHONELAMPMODE_ Constants</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetlamp">TSPI_phoneGetLamp</a>