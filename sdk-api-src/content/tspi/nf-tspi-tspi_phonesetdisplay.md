---
UID: NF:tspi.TSPI_phoneSetDisplay
title: TSPI_phoneSetDisplay function (tspi.h)
description: The TSPI_phoneSetDisplay function causes the specified string to be displayed on the specified open phone device.
helpviewer_keywords: ["TSPI_phoneSetDisplay","TSPI_phoneSetDisplay function [TAPI 2.2]","_tspi_tspi_phonesetdisplay","tspi.tspi_phonesetdisplay","tspi/TSPI_phoneSetDisplay"]
old-location: tspi\tspi_phonesetdisplay.htm
tech.root: tapi3
ms.assetid: c320122c-037a-40f5-8314-6aa3352cc994
ms.date: 12/05/2018
ms.keywords: TSPI_phoneSetDisplay, TSPI_phoneSetDisplay function [TAPI 2.2], _tspi_tspi_phonesetdisplay, tspi.tspi_phonesetdisplay, tspi/TSPI_phoneSetDisplay
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
 - TSPI_phoneSetDisplay
 - tspi/TSPI_phoneSetDisplay
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
 - TSPI_phoneSetDisplay
---

# TSPI_phoneSetDisplay function


## -description

The 
<b>TSPI_phoneSetDisplay</b> function causes the specified string to be displayed on the specified open phone device.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdPhone

The handle to the phone on which the string is to be displayed.

### -param dwRow

The row on the display where the new text is to be displayed.

### -param dwColumn

The column position on the display where the new text is to be displayed.

### -param lpsDisplay

A pointer to the memory location where the display content is stored. The application stores the display information in the format specified as <b>dwStringFormat</b> in the phone's 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure.

### -param dwSize

The size in bytes, including the <b>null</b> terminator, of the information pointed to by <i>lpDisplay</i>.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPARAM, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.

## -remarks

The specified display information is written to the phone's display, starting at the specified positions. This operation overwrites previously displayed information. If the amount of information exceeds the size of the display, the information is truncated. The amount of information that can be displayed is at most (<b>dwNumRows</b> * <b>dwNumColumns</b>) elements in size. The <b>dwNumRows</b> and <b>dwNumColumns</b> members are available in the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure returned by 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>; they are zero-based.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdevcaps">TSPI_phoneGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetdisplay">TSPI_phoneGetDisplay</a>