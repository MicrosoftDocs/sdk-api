---
UID: NF:tspi.TSPI_phoneSetButtonInfo
title: TSPI_phoneSetButtonInfo function (tspi.h)
description: The TSPI_phoneSetButtonInfo function sets information about the specified button on the specified phone.
helpviewer_keywords: ["TSPI_phoneSetButtonInfo","TSPI_phoneSetButtonInfo function [TAPI 2.2]","_tspi_tspi_phonesetbuttoninfo","tspi.tspi_phonesetbuttoninfo","tspi/TSPI_phoneSetButtonInfo"]
old-location: tspi\tspi_phonesetbuttoninfo.htm
tech.root: tapi3
ms.assetid: 33b01ac2-cbfd-4697-b242-a7a8f5d1b256
ms.date: 12/05/2018
ms.keywords: TSPI_phoneSetButtonInfo, TSPI_phoneSetButtonInfo function [TAPI 2.2], _tspi_tspi_phonesetbuttoninfo, tspi.tspi_phonesetbuttoninfo, tspi/TSPI_phoneSetButtonInfo
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
 - TSPI_phoneSetButtonInfo
 - tspi/TSPI_phoneSetButtonInfo
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
 - TSPI_phoneSetButtonInfo
---

# TSPI_phoneSetButtonInfo function


## -description

The 
<b>TSPI_phoneSetButtonInfo</b> function sets information about the specified button on the specified phone.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request. The service provider returns this value if the function completes asynchronously.

### -param hdPhone

The handle to the phone for which button info is to be set.

### -param dwButtonLampID

A button on the phone device.

### -param lpButtonInfo

A pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo">PHONEBUTTONINFO</a>. This data structure describes the mode and function, and provides additional descriptive text to be set for the button.

## -returns

Returns the (positive) <i>dwRequestID</i> value if the function is completed asynchronously, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALBUTTONLAMPID, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL.

## -remarks

This function sets the meaning and associated descriptive text of a phone's buttons.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo">PHONEBUTTONINFO</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetbuttoninfo">TSPI_phoneGetButtonInfo</a>