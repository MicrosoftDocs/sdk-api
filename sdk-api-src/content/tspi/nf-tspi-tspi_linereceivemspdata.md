---
UID: NF:tspi.TSPI_lineReceiveMSPData
title: TSPI_lineReceiveMSPData function (tspi.h)
description: The TSPI_lineReceiveMSPData function service provider receives data sent by the media service provider (MSP). This function requires TAPI 3.0 version negotiation.
helpviewer_keywords: ["TSPI_lineReceiveMSPData","TSPI_lineReceiveMSPData function [TAPI 2.2]","_tspi_tspi_linereceivemspdata","tspi.tspi_linereceivemspdata","tspi/TSPI_lineReceiveMSPData"]
old-location: tspi\tspi_linereceivemspdata.htm
tech.root: tapi3
ms.assetid: 90d334e7-e91d-482e-bd79-4b610fe5144d
ms.date: 12/05/2018
ms.keywords: TSPI_lineReceiveMSPData, TSPI_lineReceiveMSPData function [TAPI 2.2], _tspi_tspi_linereceivemspdata, tspi.tspi_linereceivemspdata, tspi/TSPI_lineReceiveMSPData
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
 - TSPI_lineReceiveMSPData
 - tspi/TSPI_lineReceiveMSPData
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
 - TSPI_lineReceiveMSPData
---

# TSPI_lineReceiveMSPData function


## -description

The 
<b>TSPI_lineReceiveMSPData</b> function service provider receives data sent by the media service provider (MSP). This function requires TAPI 3.0 version negotiation.

## -parameters

### -param hdLine

Handle to line device.

### -param hdCall

Handle for call.

### -param hdMSPLine

MSP handle for the call.

### -param pBuffer

Pointer to buffer containing MSP data.

### -param dwSize

Size of MSP data buffer.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

## -see-also

<a href="/windows/desktop/Tapi/about-the-media-service-provider-msp-">About The Media Service Provider (MSP)</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineclosemspinstance">TSPI_lineCloseMSPInstance</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linecreatemspinstance">TSPI_lineCreateMSPInstance</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemspidentify">TSPI_lineMSPIdentify</a>