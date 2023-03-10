---
UID: NF:tspi.TSPI_lineCloseMSPInstance
title: TSPI_lineCloseMSPInstance function (tspi.h)
description: The TSPI_lineCloseMSPInstance function directs the TAPI 3 DLL to close a media service provider (MSP) call instance. This function requires TAPI 3.0 version negotiation.
helpviewer_keywords: ["TSPI_lineCloseMSPInstance","TSPI_lineCloseMSPInstance function [TAPI 2.2]","_tspi_tspi_lineclosemspinstance","tspi.tspi_lineclosemspinstance","tspi/TSPI_lineCloseMSPInstance"]
old-location: tspi\tspi_lineclosemspinstance.htm
tech.root: tapi3
ms.assetid: 700824ed-05a1-4fb5-adf1-491e1dea7bf4
ms.date: 12/05/2018
ms.keywords: TSPI_lineCloseMSPInstance, TSPI_lineCloseMSPInstance function [TAPI 2.2], _tspi_tspi_lineclosemspinstance, tspi.tspi_lineclosemspinstance, tspi/TSPI_lineCloseMSPInstance
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
 - TSPI_lineCloseMSPInstance
 - tspi/TSPI_lineCloseMSPInstance
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
 - TSPI_lineCloseMSPInstance
---

# TSPI_lineCloseMSPInstance function


## -description

The 
<b>TSPI_lineCloseMSPInstance</b> function directs the TAPI 3 DLL to close a media service provider (MSP) call instance. This function requires TAPI 3.0 version negotiation.

## -parameters

### -param hdMSPLine

Pointer to the TSP handle for the MSP call.

## -returns

LINEERR_INVALPOINTER, NOERROR.

## -remarks

An MSP instance is associated with a particular application. If multiple applications are running, each TSP line may have multiple MSP instances.

## -see-also

<a href="/windows/desktop/Tapi/about-the-media-service-provider-msp-">About The Media Service Provider (MSP)</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linecreatemspinstance">TSPI_lineCreateMSPInstance</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemspidentify">TSPI_lineMSPIdentify</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linereceivemspdata">TSPI_lineReceiveMSPData</a>