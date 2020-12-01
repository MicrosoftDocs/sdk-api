---
UID: NF:tapi.phoneSetDisplay
title: phoneSetDisplay function (tapi.h)
description: The phoneSetDisplay function causes the specified string to be displayed on the specified open phone device.
helpviewer_keywords: ["_tapi2_phonesetdisplay","phoneSetDisplay","phoneSetDisplay function [TAPI 2.2]","tapi/phoneSetDisplay","tapi2.phonesetdisplay"]
old-location: tapi2\phonesetdisplay.htm
tech.root: tapi3
ms.assetid: 154efb07-7c4e-47f0-8a14-e2fe404efcb7
ms.date: 12/05/2018
ms.keywords: _tapi2_phonesetdisplay, phoneSetDisplay, phoneSetDisplay function [TAPI 2.2], tapi/phoneSetDisplay, tapi2.phonesetdisplay
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
 - phoneSetDisplay
 - tapi/phoneSetDisplay
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
 - phoneSetDisplay
---

# phoneSetDisplay function


## -description

The 
<b>phoneSetDisplay</b> function causes the specified string to be displayed on the specified open phone device.

## -parameters

### -param hPhone

Handle to the open phone device. The application must be the owner of the phone.

### -param dwRow

Row position on the display where the new text is to be displayed.

### -param dwColumn

Column position on the display where the new text is to be displayed.

### -param lpsDisplay

Pointer to the memory location where the display content is stored. The display information must have the format specified in the <b>dwStringFormat</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure, which describes the phone's device capabilities.

### -param dwSize

Size of the information pointed to by <i>lpsDisplay</i>, in bytes. If the <i>lpsDisplay</i> parameter is a pointer to a string, the size must include the null terminator.

## -returns

Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOTOWNER, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_UNINITIALIZED, PHONEERR_INVALPOINTER, PHONEERR_NOMEM, PHONEERR_INVALPARAM, PHONEERR_RESOURCEUNAVAIL.

## -remarks

The specified display information is written to the phone's display, starting at the specified positions. This operation overwrites previously displayed information. If the amount of information exceeds the size of the display, the information is truncated. The amount of information that can be displayed is at most (<b>dwNumRows</b> * <b>dwNumColumns</b>) elements in size. <b>dwNumRows</b> and <b>dwNumColumns</b> are available in the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure, which is returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetdevcaps">phoneGetDevCaps</a>; they are zero-based.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/Tapi/phone-reply">PHONE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetdevcaps">phoneGetDevCaps</a>