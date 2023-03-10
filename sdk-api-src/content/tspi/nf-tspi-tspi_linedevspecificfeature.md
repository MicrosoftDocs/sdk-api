---
UID: NF:tspi.TSPI_lineDevSpecificFeature
title: TSPI_lineDevSpecificFeature function (tspi.h)
description: The TSPI_lineDevSpecificFeature function is used as an extension mechanism to enable service providers to provide access to features not described in other operations.
helpviewer_keywords: ["TSPI_lineDevSpecificFeature","TSPI_lineDevSpecificFeature function [TAPI 2.2]","_tspi_tspi_linedevspecificfeature","tspi.tspi_linedevspecificfeature","tspi/TSPI_lineDevSpecificFeature"]
old-location: tspi\tspi_linedevspecificfeature.htm
tech.root: tapi3
ms.assetid: 0c42d932-f359-4557-bf26-daecca48781b
ms.date: 12/05/2018
ms.keywords: TSPI_lineDevSpecificFeature, TSPI_lineDevSpecificFeature function [TAPI 2.2], _tspi_tspi_linedevspecificfeature, tspi.tspi_linedevspecificfeature, tspi/TSPI_lineDevSpecificFeature
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
 - TSPI_lineDevSpecificFeature
 - tspi/TSPI_lineDevSpecificFeature
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
 - TSPI_lineDevSpecificFeature
---

# TSPI_lineDevSpecificFeature function


## -description

The 
<b>TSPI_lineDevSpecificFeature</b> function is used as an extension mechanism to enable service providers to provide access to features not described in other operations. The meanings of these extensions are device specific, and taking advantage of these extensions requires TAPI or its client application to be fully aware of them.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdLine

The service provider's handle to the line device.

### -param dwFeature

The feature to invoke on the line device. This parameter uses 
<a href="/windows/desktop/Tapi/phonebuttonfunction--constants">PHONEBUTTONFUNCTION_ constants</a>.

### -param lpParams

A pointer to a memory area used to hold a feature-dependent parameter block. The format of this parameter block is device specific.

### -param dwSize

The size of the buffer in bytes. If the <i>lpParams</i> parameter is a pointer to a string, the size must include the null terminator.

## -returns

Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALFEATURE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

Additional return values are device specific. The call state of <i>hdCall</i> is device-specific.

This function provides TAPI applications with phone feature button emulation capabilities. When TAPI invokes this operation on behalf of a client application, it specifies the equivalent of a "button press" event. This method of invoking features is highly device dependent, as the API does not define their meaning. When an application relies on device-specific extensions, the application does not port well to other service provider environments.

This function is called in direct response to an application calling the TAPI 
<a href="/windows/desktop/api/tapi/nf-tapi-linedevspecificfeature">lineDevSpecificFeature</a> function. TAPI translates the <i>hLine</i> parameter used at the TAPI level to the corresponding <i>hdLine</i> parameter used at the TSPI level. The <i>lpParams</i> buffer is passed through unmodified.

<div class="alert"><b>Note</b>  The <i>lpParams</i> data structure should not contain any pointers because they are not properly translated (thunked) when running a 16-bit application in a 32-bit version of TAPI and vice versa.</div>
<div> </div>
This operation is part of the Extended Telephony services. It only provides access to a device-specific feature without defining its meaning. This operation is only available if TAPI has successfully negotiated and selected a device-specific extension version.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)">LINE_DEVSPECIFICFEATURE</a>



<a href="/windows/desktop/Tapi/phonebuttonfunction--constants">PHONEBUTTONFUNCTION_ Constants</a>