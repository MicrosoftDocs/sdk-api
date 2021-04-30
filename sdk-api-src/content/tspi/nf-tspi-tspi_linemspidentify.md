---
UID: NF:tspi.TSPI_lineMSPIdentify
title: TSPI_lineMSPIdentify function (tspi.h)
description: The TSPI_lineMSPIdentify function determines the associated MSP CLSID for every line. This function requires TAPI 3.0 version negotiation.
helpviewer_keywords: ["TSPI_lineMSPIdentify","TSPI_lineMSPIdentify function [TAPI 2.2]","_tspi_tspi_linemspidentify","tspi.tspi_linemspidentify","tspi/TSPI_lineMSPIdentify"]
old-location: tspi\tspi_linemspidentify.htm
tech.root: tapi3
ms.assetid: a4fe8d2e-7257-49de-b5d1-e343cadad59a
ms.date: 12/05/2018
ms.keywords: TSPI_lineMSPIdentify, TSPI_lineMSPIdentify function [TAPI 2.2], _tspi_tspi_linemspidentify, tspi.tspi_linemspidentify, tspi/TSPI_lineMSPIdentify
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
 - TSPI_lineMSPIdentify
 - tspi/TSPI_lineMSPIdentify
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
 - TSPI_lineMSPIdentify
---

# TSPI_lineMSPIdentify function


## -description

The 
<b>TSPI_lineMSPIdentify</b> function determines the associated MSP CLSID for every line. This function requires TAPI 3.0 version negotiation.

## -parameters

### -param dwDeviceID

The line device whose CLSID is requested.

### -param pCLSID

The TSP fills in the CLSID of the MSP to be created for the line device indicated in <i>dwDeviceID</i>.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

## -remarks

Note that TAPI 3 calls 
<b>TSPI_lineMSPIdentify</b> only if the LINEDEVCAPFLAGS_MSP flag is set in the TSP. (You can set 
<a href="/windows/desktop/Tapi/linedevcapflags--constants">LINEDEVCAPFLAGS_constants</a> in the <b>dwDevCapFlags</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure.)

If the device does not have an associated MSP, the TSP returns LINEERR_OPERATIONUNAVAIL.

## -see-also

<a href="/windows/desktop/Tapi/about-the-media-service-provider-msp-">About The Media Service Provider (MSP)</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineclosemspinstance">TSPI_lineCloseMSPInstance</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linecreatemspinstance">TSPI_lineCreateMSPInstance</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linereceivemspdata">TSPI_lineReceiveMSPData</a>