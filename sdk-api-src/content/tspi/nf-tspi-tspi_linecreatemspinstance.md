---
UID: NF:tspi.TSPI_lineCreateMSPInstance
title: TSPI_lineCreateMSPInstance function (tspi.h)
description: The TSPI_lineCreateMSPInstance function directs the TAPI 3 DLL to create a media service provider (MSP) instance for a specific line device. This function returns a TSP handle for the MSP call. This function requires TAPI 3.0 version negotiation.
helpviewer_keywords: ["TSPI_lineCreateMSPInstance","TSPI_lineCreateMSPInstance function [TAPI 2.2]","_tspi_tspi_linecreatemspinstance","tspi.tspi_linecreatemspinstance","tspi/TSPI_lineCreateMSPInstance"]
old-location: tspi\tspi_linecreatemspinstance.htm
tech.root: tapi3
ms.assetid: 1d3421d8-2ef8-4f62-b6b0-5671a18ffc0b
ms.date: 12/05/2018
ms.keywords: TSPI_lineCreateMSPInstance, TSPI_lineCreateMSPInstance function [TAPI 2.2], _tspi_tspi_linecreatemspinstance, tspi.tspi_linecreatemspinstance, tspi/TSPI_lineCreateMSPInstance
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
 - TSPI_lineCreateMSPInstance
 - tspi/TSPI_lineCreateMSPInstance
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
 - TSPI_lineCreateMSPInstance
---

# TSPI_lineCreateMSPInstance function


## -description

The 
<b>TSPI_lineCreateMSPInstance</b> function directs the TAPI 3 DLL to create a media service provider (MSP) instance for a specific line device. This function returns a TSP handle for the MSP call. This function requires TAPI 3.0 version negotiation.

## -parameters

### -param hdLine

The service provider's handle to the line.

### -param dwAddressID

An address on the specified open line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param htMSPLine

The TAPI handle for the MSP call.

### -param lphdMSPLine

Pointer to the TSP handle for the MSP call.

## -returns

LINEERR_INVALLINEHANDLE, LINEERR_INVALPOINTER, NOERROR

## -remarks

The service provider should save the <i>htMSPLine</i> handle field, to be used when sending 
<a href="/windows/desktop/Tapi/line-sendmspdata">LINE_SENDMSPDATA</a> messages to TAPISRV.

An MSP instance is associated with a particular application. If multiple applications are running, each TSP line may have multiple MSP instances.

## -see-also

<a href="/windows/desktop/Tapi/about-the-media-service-provider-msp-">About The Media Service Provider (MSP)</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineclosemspinstance">TSPI_lineCloseMSPInstance</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemspidentify">TSPI_lineMSPIdentify</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linereceivemspdata">TSPI_lineReceiveMSPData</a>