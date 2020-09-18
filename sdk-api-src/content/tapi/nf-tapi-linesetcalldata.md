---
UID: NF:tapi.lineSetCallData
title: lineSetCallData function (tapi.h)
description: The lineSetCallData function sets the CallData member in LINECALLINFO.
helpviewer_keywords: ["_tapi2_linesetcalldata","lineSetCallData","lineSetCallData function [TAPI 2.2]","tapi/lineSetCallData","tapi2.linesetcalldata"]
old-location: tapi2\linesetcalldata.htm
tech.root: tapi3
ms.assetid: f428f952-f8ff-4b55-a957-58fdb35a8c0e
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetcalldata, lineSetCallData, lineSetCallData function [TAPI 2.2], tapi/lineSetCallData, tapi2.linesetcalldata
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
 - lineSetCallData
 - tapi/lineSetCallData
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
 - lineSetCallData
---

# lineSetCallData function


## -description

The 
<b>lineSetCallData</b> function sets the <b>CallData</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>. Depending on the service provider implementation, the <b>CallData</b> member can be propagated to all applications having handles to the call, including those on other machines (through the server), and can travel with the call when it is transferred.

## -parameters

### -param hCall

Handle to the call. The application must have OWNER privilege.

### -param lpCallData

Address of the data to be copied to the <b>CallData</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>, replacing any existing data. For more information, see the 
<a href="/windows/desktop/Tapi/call-data-ovr">call data</a> topic.

### -param dwSize

Number of bytes of data to be copied. A value of 0 causes any existing data to be removed. 




<div class="alert"><b>Note</b>  If <i>lpCallData</i> is a pointer to a string, the size must include the null terminator.</div>
<div> </div>

## -returns

Returns a positive request identifier if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALCALLHANDLE, LINEERR_INVALCALLSTATE, LINEERR_INVALPARAM, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_NOTOWNER, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>