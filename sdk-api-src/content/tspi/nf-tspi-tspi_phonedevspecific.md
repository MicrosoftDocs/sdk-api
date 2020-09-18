---
UID: NF:tspi.TSPI_phoneDevSpecific
title: TSPI_phoneDevSpecific function (tspi.h)
description: The TSPI_phoneDevSpecific function is used as a general extension mechanism to enable a Telephony API implementation to provide features not described in the other operations. The meanings of these extensions are device specific.
helpviewer_keywords: ["TSPI_phoneDevSpecific","TSPI_phoneDevSpecific function [TAPI 2.2]","_tspi_tspi_phonedevspecific","tspi.tspi_phonedevspecific","tspi/TSPI_phoneDevSpecific"]
old-location: tspi\tspi_phonedevspecific.htm
tech.root: tapi3
ms.assetid: 8c2161c2-ab7c-44b0-a7a0-249412359838
ms.date: 12/05/2018
ms.keywords: TSPI_phoneDevSpecific, TSPI_phoneDevSpecific function [TAPI 2.2], _tspi_tspi_phonedevspecific, tspi.tspi_phonedevspecific, tspi/TSPI_phoneDevSpecific
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
 - TSPI_phoneDevSpecific
 - tspi/TSPI_phoneDevSpecific
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
 - TSPI_phoneDevSpecific
---

# TSPI_phoneDevSpecific function


## -description

The 
<b>TSPI_phoneDevSpecific</b> function is used as a general extension mechanism to enable a Telephony API implementation to provide features not described in the other operations. The meanings of these extensions are device specific.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdPhone

The handle to the phone on which a device-specific operation is to be performed.

### -param lpParams

A pointer to a memory area used to hold a parameter block. Its interpretation is device specific. The <i>lpParams</i> parameter should not contain pointers. To get information back to the application from 
<b>TSPI_phoneDevSpecific</b>, the service provider sends a 
<a href="/previous-versions/windows/desktop/legacy/ms725258(v=vs.85)">PHONE_DEVSPECIFIC</a> message with the information.

### -param dwSize

The size in bytes of the parameter block area.

## -returns

Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or it is an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_NOMEM, PHONEERR_OPERATIONFAILED, PHONEERR_RESOURCEUNAVAIL.

## -remarks

Additional return values are device specific.

This operation provides a generic parameter profile. The interpretation of the parameter block is device specific. Indications and replies that are device specific should use the 
<a href="/previous-versions/windows/desktop/legacy/ms725258(v=vs.85)">PHONE_DEVSPECIFIC</a> message.

This function is called in direct response to an application that has called the TAPI 
<a href="/windows/desktop/api/tapi/nf-tapi-phonedevspecific">phoneDevSpecific</a> function. TAPI translates the <i>hPhone</i> parameter used at the TAPI level to the corresponding <i>hdPhone</i> parameter used at the TSPI level. The <i>lpParams</i> buffer is passed through unmodified.

A service provider can provide access to device-specific functions by defining parameters for use with this operation. Applications that want to make use of these device-specific extensions should consult the device-specific (vendor-specific) documentation that describes what extensions are defined.

<div class="alert"><b>Note</b>  An application that relies on these device-specific extensions is typically not portable in working with other service provider environments.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/previous-versions/windows/desktop/legacy/ms725258(v=vs.85)">PHONE_DEVSPECIFIC</a>