---
UID: NF:tspi.TSPI_lineCreateMSPInstance
title: TSPI_lineCreateMSPInstance function
author: windows-sdk-content
description: The TSPI_lineCreateMSPInstance function directs the TAPI 3 DLL to create a media service provider (MSP) instance for a specific line device. This function returns a TSP handle for the MSP call. This function requires TAPI 3.0 version negotiation.
old-location: tspi\tspi_linecreatemspinstance.htm
tech.root: TAPI
ms.assetid: 1d3421d8-2ef8-4f62-b6b0-5671a18ffc0b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: TSPI_lineCreateMSPInstance, TSPI_lineCreateMSPInstance function [TAPI 2.2], _tspi_tspi_linecreatemspinstance, tspi.tspi_linecreatemspinstance, tspi/TSPI_lineCreateMSPInstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineCreateMSPInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/982f40b3-7758-493c-9d04-6480e3c9e86d">LINE_SENDMSPDATA</a> messages to TAPISRV.

An MSP instance is associated with a particular application. If multiple applications are running, each TSP line may have multiple MSP instances.




## -see-also




<a href="https://msdn.microsoft.com/2dd1268f-b31a-443b-a36b-05c1570e7a8a">About The Media Service Provider (MSP)</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/700824ed-05a1-4fb5-adf1-491e1dea7bf4">TSPI_lineCloseMSPInstance</a>



<a href="https://msdn.microsoft.com/a4fe8d2e-7257-49de-b5d1-e343cadad59a">TSPI_lineMSPIdentify</a>



<a href="https://msdn.microsoft.com/90d334e7-e91d-482e-bd79-4b610fe5144d">TSPI_lineReceiveMSPData</a>
 

 

