---
UID: NF:tapi.phoneGetData
title: phoneGetData function (tapi.h)
description: The phoneGetData function uploads the information from the specified location in the open phone device to the specified buffer.
helpviewer_keywords: ["_tapi2_phonegetdata","phoneGetData","phoneGetData function [TAPI 2.2]","tapi/phoneGetData","tapi2.phonegetdata"]
old-location: tapi2\phonegetdata.htm
tech.root: tapi3
ms.assetid: 9ad2f99e-73b3-4e4c-a6cd-49ca0fe775ca
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegetdata, phoneGetData, phoneGetData function [TAPI 2.2], tapi/phoneGetData, tapi2.phonegetdata
req.header: tapi.h
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - phoneGetData
 - tapi/phoneGetData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - phoneGetData
---

# phoneGetData function


## -description

The 
<b>phoneGetData</b> function uploads the information from the specified location in the open phone device to the specified buffer.

## -parameters

### -param hPhone

Handle to the open phone device.

### -param dwDataID

Where in the phone device the buffer is to be uploaded from.

### -param lpData

Pointer to the memory buffer where the data is to be uploaded.

### -param dwSize

Size of the data buffer, in bytes.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALDATAID, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.

## -remarks

The function uploads a maximum of <i>dwSize</i> bytes from the phone device into the memory area pointed to by <i>lpData</i>. If <i>dwSize</i> is zero, nothing is copied. The size of each data area is listed in the phone's device capabilities.

## -see-also

<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>