---
UID: NF:tspi.TSPI_lineReceiveMSPData
title: TSPI_lineReceiveMSPData function
author: windows-sdk-content
description: The TSPI_lineReceiveMSPData function service provider receives data sent by the media service provider (MSP). This function requires TAPI 3.0 version negotiation.
old-location: tspi\tspi_linereceivemspdata.htm
old-project: Tapi
ms.assetid: 90d334e7-e91d-482e-bd79-4b610fe5144d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: TSPI_lineReceiveMSPData, TSPI_lineReceiveMSPData function [TAPI 2.2], _tspi_tspi_linereceivemspdata, tspi.tspi_linereceivemspdata, tspi/TSPI_lineReceiveMSPData
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineReceiveMSPData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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




<a href="https://msdn.microsoft.com/2dd1268f-b31a-443b-a36b-05c1570e7a8a">About The Media Service Provider (MSP)</a>



<a href="https://msdn.microsoft.com/700824ed-05a1-4fb5-adf1-491e1dea7bf4">TSPI_lineCloseMSPInstance</a>



<a href="https://msdn.microsoft.com/1d3421d8-2ef8-4f62-b6b0-5671a18ffc0b">TSPI_lineCreateMSPInstance</a>



<a href="https://msdn.microsoft.com/a4fe8d2e-7257-49de-b5d1-e343cadad59a">TSPI_lineMSPIdentify</a>
 

 

