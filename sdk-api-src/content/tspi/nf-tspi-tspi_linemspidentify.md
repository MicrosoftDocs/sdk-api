---
UID: NF:tspi.TSPI_lineMSPIdentify
title: TSPI_lineMSPIdentify function
author: windows-sdk-content
description: The TSPI_lineMSPIdentify function determines the associated MSP CLSID for every line. This function requires TAPI 3.0 version negotiation.
old-location: tspi\tspi_linemspidentify.htm
tech.root: tapi
ms.assetid: a4fe8d2e-7257-49de-b5d1-e343cadad59a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TSPI_lineMSPIdentify, TSPI_lineMSPIdentify function [TAPI 2.2], _tspi_tspi_linemspidentify, tspi.tspi_linemspidentify, tspi/TSPI_lineMSPIdentify
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
 - TSPI_lineMSPIdentify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/0c537488-9fb9-4961-bd0a-1937aefc0b08">LINEDEVCAPFLAGS_constants</a> in the <b>dwDevCapFlags</b> member of the 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> structure.)

If the device does not have an associated MSP, the TSP returns LINEERR_OPERATIONUNAVAIL.




## -see-also




<a href="https://msdn.microsoft.com/2dd1268f-b31a-443b-a36b-05c1570e7a8a">About The Media Service Provider (MSP)</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/700824ed-05a1-4fb5-adf1-491e1dea7bf4">TSPI_lineCloseMSPInstance</a>



<a href="https://msdn.microsoft.com/1d3421d8-2ef8-4f62-b6b0-5671a18ffc0b">TSPI_lineCreateMSPInstance</a>



<a href="https://msdn.microsoft.com/90d334e7-e91d-482e-bd79-4b610fe5144d">TSPI_lineReceiveMSPData</a>
 

 

