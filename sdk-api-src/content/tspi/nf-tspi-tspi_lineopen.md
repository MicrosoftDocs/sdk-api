---
UID: NF:tspi.TSPI_lineOpen
title: TSPI_lineOpen function
author: windows-sdk-content
description: The TSPI_lineOpen function opens the line device whose device identifier is given, returning the service provider's handle for the device.
old-location: tspi\tspi_lineopen.htm
old-project: Tapi
ms.assetid: 97cde843-65bc-46ae-a6ae-724f2c9c5217
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: TSPI_lineOpen, TSPI_lineOpen function [TAPI 2.2], _tspi_tspi_lineopen, tspi.tspi_lineopen, tspi/TSPI_lineOpen
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
 - TSPI_lineOpen
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_lineOpen function


## -description


The 
<b>TSPI_lineOpen</b> function opens the line device whose device identifier is given, returning the service provider's handle for the device. The service provider must retain the TAPI handle for the device for use in subsequent calls to the 
<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">LINEEVENT</a> callback procedure.


## -parameters




### -param dwDeviceID

Identifies the line device to be opened.


### -param htLine

The TAPI handle for the line device to be used in subsequent calls to the 
<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">LINEEVENT</a> callback procedure to identify the device.


### -param lphdLine

A pointer to an 
<a href="https://msdn.microsoft.com/8bb1c3fe-a3de-4299-bc15-58321c5da549">HDRVLINE</a> where the service provider fills in its handle for the line device.


### -param dwTSPIVersion

The TSPI version.


### -param lpfnEventProc

A pointer to the 
<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">LINEEVENT</a> callback procedure supplied by TAPI that the service provider calls to report subsequent events on the line.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_ALLOCATED, LINEERR_OPERATIONUNAVAIL, LINEERR_NODRIVER, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.




## -remarks



The service provider should reserve any non-sharable resources that are required to manage the line. However, any actions that can be postponed to 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> should be. It is a design assumption in TAPI that 
<a href="https://msdn.microsoft.com/7dd39866-0b3e-47be-8aa8-adfb66df6644">lineOpen</a> is an "inexpensive" operation. For example, if the line is opened in monitor mode only, it should not be necessary for a COMM-port-based service provider to open the COMM port.

This procedure does not correspond directly to any procedure at the TAPI level, at which the functions of enabling device-specific extensions, selecting line characteristics, and setting media type detection are included in the functionality defined by 
<a href="https://msdn.microsoft.com/7dd39866-0b3e-47be-8aa8-adfb66df6644">lineOpen</a>. At the TSPI level, these additional capabilities are separated out into 
<a href="https://msdn.microsoft.com/cd7cc421-3efb-4fe1-858c-4d894f4d9377">TSPI_lineNegotiateExtVersion</a>, 
<a href="https://msdn.microsoft.com/407fa545-6890-4a8c-b5a8-bddeacc46e18">TSPI_lineSetDefaultMediaDetection</a> and 
<a href="https://msdn.microsoft.com/8fa3f9ab-1749-43c8-b2a5-c481b1f94177">TSPI_lineConditionalMediaDetection</a>.




## -see-also




<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">LINEEVENT</a>



<a href="https://msdn.microsoft.com/0344151e-3f40-472d-84c2-906291777da6">LINE_CLOSE</a>



<a href="https://msdn.microsoft.com/d1041620-609b-476b-bdb7-e1e0cebd74f1">TSPI_lineClose</a>



<a href="https://msdn.microsoft.com/8fa3f9ab-1749-43c8-b2a5-c481b1f94177">TSPI_lineConditionalMediaDetection</a>



<a href="https://msdn.microsoft.com/cd7cc421-3efb-4fe1-858c-4d894f4d9377">TSPI_lineNegotiateExtVersion</a>



<a href="https://msdn.microsoft.com/d92fbf18-282d-485b-9d56-22e4896ece57">TSPI_lineNegotiateTSPIVersion</a>



<a href="https://msdn.microsoft.com/407fa545-6890-4a8c-b5a8-bddeacc46e18">TSPI_lineSetDefaultMediaDetection</a>
 

 

