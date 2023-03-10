---
UID: NF:tspi.TSPI_phoneSetData
title: TSPI_phoneSetData function (tspi.h)
description: The TSPI_phoneSetData function downloads the information in the specified buffer to the opened phone device at the selected data identifier.
helpviewer_keywords: ["TSPI_phoneSetData","TSPI_phoneSetData function [TAPI 2.2]","_tspi_tspi_phonesetdata","tspi.tspi_phonesetdata","tspi/TSPI_phoneSetData"]
old-location: tspi\tspi_phonesetdata.htm
tech.root: tapi3
ms.assetid: c4861878-639b-45a5-aff8-3f1fd1a2e153
ms.date: 12/05/2018
ms.keywords: TSPI_phoneSetData, TSPI_phoneSetData function [TAPI 2.2], _tspi_tspi_phonesetdata, tspi.tspi_phonesetdata, tspi/TSPI_phoneSetData
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
 - TSPI_phoneSetData
 - tspi/TSPI_phoneSetData
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
 - TSPI_phoneSetData
---

# TSPI_phoneSetData function


## -description

The 
<b>TSPI_phoneSetData</b> function downloads the information in the specified buffer to the opened phone device at the selected data identifier.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdPhone

The handle to the phone into which data is to be downloaded.

### -param dwDataID

Specifies where in the phone device the buffer is to be downloaded.

### -param lpData

A pointer to the memory location where the data is to be downloaded from.

### -param dwSize

The size of the buffer in bytes. If the <i>lpData</i> parameter is a pointer to a string, the size must include the <b>null</b> terminator.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALDATAID, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.

## -remarks

The function downloads a maximum of <i>dwSize</i> bytes from <i>lpData</i> to the phone device. The format of the data, its meaning to the phone device, and the meaning of the data identifier are service-provider specific. The data in the buffer or the selection of a data identifier can act as commands to the phone device.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdata">TSPI_phoneGetData</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>