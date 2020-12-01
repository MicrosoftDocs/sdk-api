---
UID: NF:tspi.TSPI_phoneGetExtensionID
title: TSPI_phoneGetExtensionID function (tspi.h)
description: The TSPI_phoneGetExtensionID function retrieves the extension identifier that the service provider supports for the indicated phone device.
helpviewer_keywords: ["TSPI_phoneGetExtensionID","TSPI_phoneGetExtensionID function [TAPI 2.2]","_tspi_tspi_phonegetextensionid","tspi.tspi_phonegetextensionid","tspi/TSPI_phoneGetExtensionID"]
old-location: tspi\tspi_phonegetextensionid.htm
tech.root: tapi3
ms.assetid: c4c1c68f-0a48-40f2-8eb9-f54c3572578c
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetExtensionID, TSPI_phoneGetExtensionID function [TAPI 2.2], _tspi_tspi_phonegetextensionid, tspi.tspi_phonegetextensionid, tspi/TSPI_phoneGetExtensionID
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
 - TSPI_phoneGetExtensionID
 - tspi/TSPI_phoneGetExtensionID
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
 - TSPI_phoneGetExtensionID
---

# TSPI_phoneGetExtensionID function


## -description

The 
<b>TSPI_phoneGetExtensionID</b> function retrieves the extension identifier that the service provider supports for the indicated phone device.

## -parameters

### -param dwDeviceID

The phone device to be queried.

### -param dwTSPIVersion

Specifies an interface version number that is negotiated for this device using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion">TSPI_phoneNegotiateTSPIVersion</a>. This function operates according to the interface specification at this version level.

### -param lpExtensionID

A pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-phoneextensionid">PHONEEXTENSIONID</a>. If the service provider supports provider-specific extensions, it fills this structure with the extension identifier of these extensions. If the service provider does not support extensions, it fills this structure with all zeros. An extension identifier of all zeros is not a legal extension identifier, since the all-zeros value is used to indicate that the service provider does not support extensions.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_RESOURCEUNAVAIL, PHONEERR_NODRIVER, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL.

## -remarks

This function is typically called by TAPI in response to an application calling the 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a> function. The result returned by the service provider should be appropriate for use in a subsequent call to 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiateextversion">TSPI_phoneNegotiateExtVersion</a>.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phoneextensionid">PHONEEXTENSIONID</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiateextversion">TSPI_phoneNegotiateExtVersion</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion">TSPI_phoneNegotiateTSPIVersion</a>