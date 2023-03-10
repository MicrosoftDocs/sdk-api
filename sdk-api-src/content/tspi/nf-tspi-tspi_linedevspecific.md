---
UID: NF:tspi.TSPI_lineDevSpecific
title: TSPI_lineDevSpecific function (tspi.h)
description: The TSPI_lineDevSpecific function is used as a general extension mechanism to enable service providers to provide access to features not described in other operations.
helpviewer_keywords: ["TSPI_lineDevSpecific","TSPI_lineDevSpecific function [TAPI 2.2]","_tspi_tspi_linedevspecific","tspi.tspi_linedevspecific","tspi/TSPI_lineDevSpecific"]
old-location: tspi\tspi_linedevspecific.htm
tech.root: tapi3
ms.assetid: 16510976-6fa6-4e48-837a-98f94d4e1342
ms.date: 12/05/2018
ms.keywords: TSPI_lineDevSpecific, TSPI_lineDevSpecific function [TAPI 2.2], _tspi_tspi_linedevspecific, tspi.tspi_linedevspecific, tspi/TSPI_lineDevSpecific
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
 - TSPI_lineDevSpecific
 - tspi/TSPI_lineDevSpecific
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
 - TSPI_lineDevSpecific
---

# TSPI_lineDevSpecific function


## -description

The 
<b>TSPI_lineDevSpecific</b> function is used as a general extension mechanism to enable service providers to provide access to features not described in other operations. The meanings of the extensions are device-specific, and to take advantage of these extensions the application must be fully aware of them.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdLine

The service provider's handle to the line to be operated on.

### -param dwAddressID

The address on the specified line to be operated on. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param hdCall

The service provider's handle to the call to be operated on. This field may have the value <b>NULL</b>. The call state of <i>hdCall</i> is device specific.

### -param lpParams

A pointer to a memory area used to hold a parameter block. The format of this parameter block is device specific.

### -param dwSize

The size in bytes of the parameter block area. If the <i>lpParams</i> parameter is a pointer to a string, the size must include the <b>null</b> terminator.

## -returns

Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

Additional return values are device specific.

This operation provides a generic parameter profile. The interpretation of the parameter structure is device specific. TAPI always specifies the <i>hdLine</i> parameter. Whether <i>dwAddressID</i> and/or <i>hdCall</i> are expected to be valid is device specific. If specified, they must belong to <i>hdLine</i>. Indications and replies sent back to the application that are device specific use the 
<a href="/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)">LINE_DEVSPECIFIC</a> message.

This function is called in direct response to an application calling the TAPI function 
<a href="/windows/desktop/api/tapi/nf-tapi-linedevspecific">lineDevSpecific</a>. TAPI translates the <i>hLine</i> and <i>hdCall</i> parameters used at the TAPI level to the corresponding <i>hdLine</i> and <i>hdCall</i> parameters used at the TSPI level. The <i>lpParams</i> buffer is passed unmodified.

<div class="alert"><b>Note</b>  The <i>lpParams</i> data structure should not contain any pointers because they would not be properly translated (thunked) when running a 16-bit application in a 32-bit version of TAPI and vice versa.</div>
<div> </div>
A service provider can provide access to device-specific functions by defining parameters for use with this operation. Applications that want to make use of these device-specific extensions should consult the device-specific documentation (in this case meaning vendor-specific) that describes which extensions are defined.

<div class="alert"><b>Note</b>  An application that relies on device-specific extensions is not portable in working with other service provider environments. Use vendor-specific extensions.</div>
<div> </div>
This operation is part of the Extended Telephony services. It only provides access to a device-specific feature without defining its meaning. This operation is only available if the application has successfully negotiated and selected a device-specific extension version.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)">LINE_DEVSPECIFIC</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiateextversion">TSPI_lineNegotiateExtVersion</a>