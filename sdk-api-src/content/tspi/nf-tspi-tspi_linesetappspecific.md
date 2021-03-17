---
UID: NF:tspi.TSPI_lineSetAppSpecific
title: TSPI_lineSetAppSpecific function (tspi.h)
description: The TSPI_lineSetAppSpecific function sets the application-specific field of the specified call's LINECALLINFO structure.
helpviewer_keywords: ["TSPI_lineSetAppSpecific","TSPI_lineSetAppSpecific function [TAPI 2.2]","_tspi_tspi_linesetappspecific","tspi.tspi_linesetappspecific","tspi/TSPI_lineSetAppSpecific"]
old-location: tspi\tspi_linesetappspecific.htm
tech.root: tapi3
ms.assetid: aa09b03d-5e72-4db5-b21a-87841fbce70b
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetAppSpecific, TSPI_lineSetAppSpecific function [TAPI 2.2], _tspi_tspi_linesetappspecific, tspi.tspi_linesetappspecific, tspi/TSPI_lineSetAppSpecific
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
 - TSPI_lineSetAppSpecific
 - tspi/TSPI_lineSetAppSpecific
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
 - TSPI_lineSetAppSpecific
---

# TSPI_lineSetAppSpecific function


## -description

The 
<b>TSPI_lineSetAppSpecific</b> function sets the application-specific field of the specified call's 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure.

## -parameters

### -param hdCall

The handle to the call whose application-specific field is to be set. The call state of <i>hdCall</i> can be any state.

### -param dwAppSpecific

The new content of the <b>dwAppSpecific</b> member for the call's 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure. This value is uninterpreted by the service provider. This parameter is not validated by TAPI when this function is called.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_OPERATIONUNAVAIL.

## -remarks

The application-specific field in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> data structure that exists for each call is uninterpreted by the Telephony API or any of its service providers. Its usage is entirely defined by the applications. The field can be read from the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> record returned by 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a>. However, 
<b>TSPI_lineSetAppSpecific</b> must be used to set the field so that changes become visible to other applications. When this field is changed, the service provider sends a LINE_CALLINFO message with an indication that the <b>AppSpecific</b> field has changed.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)">LINE_CALLINFO</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a>