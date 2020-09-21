---
UID: NF:tapi.phoneSetData
title: phoneSetData function (tapi.h)
description: The phoneSetData function downloads the information in the specified buffer to the opened phone device at the selected data identifier.
helpviewer_keywords: ["_tapi2_phonesetdata","phoneSetData","phoneSetData function [TAPI 2.2]","tapi/phoneSetData","tapi2.phonesetdata"]
old-location: tapi2\phonesetdata.htm
tech.root: tapi3
ms.assetid: 4563467b-6577-4210-9440-8445e307ac38
ms.date: 12/05/2018
ms.keywords: _tapi2_phonesetdata, phoneSetData, phoneSetData function [TAPI 2.2], tapi/phoneSetData, tapi2.phonesetdata
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
 - phoneSetData
 - tapi/phoneSetData
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
 - phoneSetData
---

# phoneSetData function


## -description

The 
<b>phoneSetData</b> function downloads the information in the specified buffer to the opened phone device at the selected data identifier.

## -parameters

### -param hPhone

Handle to the open phone device. The application must be the owner of the phone.

### -param dwDataID

Where in the phone device the buffer is to be downloaded.

### -param lpData

Pointer to the memory location where the data is to be downloaded from.

### -param dwSize

Size of the buffer, in bytes.

## -returns

Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOTOWNER, PHONEERR_NOMEM, PHONEERR_INVALDATAID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPOINTER, PHONEERR_UNINITIALIZED.

## -remarks

The 
<b>phoneSetData</b> function downloads a maximum of <i>dwSize</i> bytes from <i>lpData</i> to the phone device. The format of the data, its meaning to the phone device, and the meaning of the data identifier are service provider-specific. The data in the buffer or the selection of a data identifier may act as commands to the phone device.

## -see-also

<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>