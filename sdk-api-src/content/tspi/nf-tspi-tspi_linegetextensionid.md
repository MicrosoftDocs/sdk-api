---
UID: NF:tspi.TSPI_lineGetExtensionID
title: TSPI_lineGetExtensionID function (tspi.h)
description: The TSPI_lineGetExtensionID function returns the extension identifier that the service provider supports for the indicated line device.
helpviewer_keywords: ["TSPI_lineGetExtensionID","TSPI_lineGetExtensionID function [TAPI 2.2]","_tspi_tspi_linegetextensionid","tspi.tspi_linegetextensionid","tspi/TSPI_lineGetExtensionID"]
old-location: tspi\tspi_linegetextensionid.htm
tech.root: tapi3
ms.assetid: aaea0a6a-bf22-491f-b1bf-d2195fba6af5
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetExtensionID, TSPI_lineGetExtensionID function [TAPI 2.2], _tspi_tspi_linegetextensionid, tspi.tspi_linegetextensionid, tspi/TSPI_lineGetExtensionID
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
 - TSPI_lineGetExtensionID
 - tspi/TSPI_lineGetExtensionID
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
 - TSPI_lineGetExtensionID
---

# TSPI_lineGetExtensionID function


## -description

The 
<b>TSPI_lineGetExtensionID</b> function returns the extension identifier that the service provider supports for the indicated line device.

## -parameters

### -param dwDeviceID

The line device to be queried.

### -param dwTSPIVersion

An interface version number that was already negotiated for this device using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiatetspiversion">TSPI_lineNegotiateTSPIVersion</a>. This function operates according to the interface specification at this version level.

### -param lpExtensionID

A pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineextensionid">LINEEXTENSIONID</a>. If the service provider supports provider-specific extensions, it fills this structure with the extension identifier of these extensions. If the service provider does not support extensions, it fills this structure with all zeros. (Therefore, a valid extension identifier cannot consist of all zeros.)

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL.

## -remarks

This function is typically called by TAPI in response to an application calling the 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a> function. The result returned by the service provider should be appropriate for use in a subsequent call to 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiateextversion">TSPI_lineNegotiateExtVersion</a>. An extension identifier of all zeros is not a legal extension identifier, because the all-zeros value is used to indicate that the service provider does not support extensions.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiateextversion">TSPI_lineNegotiateExtVersion</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiatetspiversion">TSPI_lineNegotiateTSPIVersion</a>