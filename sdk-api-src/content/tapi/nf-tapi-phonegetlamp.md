---
UID: NF:tapi.phoneGetLamp
title: phoneGetLamp function (tapi.h)
description: The phoneGetLamp function returns the current lamp mode of the specified lamp.
helpviewer_keywords: ["_tapi2_phonegetlamp","phoneGetLamp","phoneGetLamp function [TAPI 2.2]","tapi/phoneGetLamp","tapi2.phonegetlamp"]
old-location: tapi2\phonegetlamp.htm
tech.root: tapi3
ms.assetid: 97bc1dc1-ac7e-479f-8fea-e2fcca88367b
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegetlamp, phoneGetLamp, phoneGetLamp function [TAPI 2.2], tapi/phoneGetLamp, tapi2.phonegetlamp
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
 - phoneGetLamp
 - tapi/phoneGetLamp
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
 - phoneGetLamp
---

# phoneGetLamp function


## -description

The 
<b>phoneGetLamp</b> function returns the current lamp mode of the specified lamp.

## -parameters

### -param hPhone

Handle to the open phone device.

### -param dwButtonLampID

Identifier of the lamp to be queried.

### -param lpdwLampMode

Pointer to a memory location that holds the lamp mode status of the given lamp. This parameter uses one and only one of the 
<a href="/windows/desktop/Tapi/phonelampmode--constants">PHONELAMPMODE_ Constants</a>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALBUTTONLAMPID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.

## -remarks

Phone sets that have multiple lamps per button should be modeled using multiple button/lamp pairs. Each extra button/lamp pair should use a DUMMY button.

## -see-also

<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>