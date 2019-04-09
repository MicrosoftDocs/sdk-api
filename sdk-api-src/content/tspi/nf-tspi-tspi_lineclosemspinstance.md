---
UID: NF:tspi.TSPI_lineCloseMSPInstance
title: TSPI_lineCloseMSPInstance function (tspi.h)
author: windows-sdk-content
description: The TSPI_lineCloseMSPInstance function directs the TAPI 3 DLL to close a media service provider (MSP) call instance. This function requires TAPI 3.0 version negotiation.
old-location: tspi\tspi_lineclosemspinstance.htm
tech.root: Tapi
ms.assetid: 700824ed-05a1-4fb5-adf1-491e1dea7bf4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TSPI_lineCloseMSPInstance, TSPI_lineCloseMSPInstance function [TAPI 2.2], _tspi_tspi_lineclosemspinstance, tspi.tspi_lineclosemspinstance, tspi/TSPI_lineCloseMSPInstance
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
 - TSPI_lineCloseMSPInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/2dd1268f-b31a-443b-a36b-05c1570e7a8a">About The Media Service Provider (MSP)</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/1d3421d8-2ef8-4f62-b6b0-5671a18ffc0b">TSPI_lineCreateMSPInstance</a>



<a href="https://msdn.microsoft.com/a4fe8d2e-7257-49de-b5d1-e343cadad59a">TSPI_lineMSPIdentify</a>



<a href="https://msdn.microsoft.com/90d334e7-e91d-482e-bd79-4b610fe5144d">TSPI_lineReceiveMSPData</a>
 

 

