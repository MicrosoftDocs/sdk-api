---
UID: NF:tspi.TSPI_lineNegotiateExtVersion
title: TSPI_lineNegotiateExtVersion function
author: windows-sdk-content
description: The TSPI_lineNegotiateExtVersion function returns the highest extension version number the service provider can operate under for this device, given the range of possible extension versions.
old-location: tspi\tspi_linenegotiateextversion.htm
tech.root: TAPI
ms.assetid: cd7cc421-3efb-4fe1-858c-4d894f4d9377
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: TSPI_lineNegotiateExtVersion, TSPI_lineNegotiateExtVersion function [TAPI 2.2], _tspi_tspi_linenegotiateextversion, tspi.tspi_linenegotiateextversion, tspi/TSPI_lineNegotiateExtVersion
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
 - TSPI_lineNegotiateExtVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineNegotiateExtVersion function


## -description


The 
<b>TSPI_lineNegotiateExtVersion</b> function returns the highest extension version number the service provider can operate under for this device, given the range of possible extension versions.


## -parameters




### -param dwDeviceID

Identifies the line device for which interface version negotiation is to be performed. The value 
<a href="https://msdn.microsoft.com/ce978913-47a1-4387-bd1b-1795aaf82dd7">INITIALIZE_NEGOTIATION</a> may not be used for this function.


### -param dwTSPIVersion

An interface version number that has already been negotiated for this device using 
<a href="https://msdn.microsoft.com/d92fbf18-282d-485b-9d56-22e4896ece57">TSPI_lineNegotiateTSPIVersion</a>. This function operates according to the interface specification at this version level.


### -param dwLowVersion

The lowest extension version number under which TAPI or its client application can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number. TAPI does not validate this parameter when this function is called.


### -param dwHighVersion

The highest extension version number under which TAPI or its client application can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number. TAPI does not validate this parameter when this function is called.


### -param lpdwExtVersion

A pointer to a <b>DWORD</b>. Upon a successful return from this function, the service provider fills this location with the highest extension version number, within the range requested by the caller, under which the service provider can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number. If the requested range does not overlap the range supported by the service provider, the function returns LINEERR_INCOMPATIBLEEXTVERSION.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_OPERATIONUNAVAIL, LINEERR_INCOMPATIBLEEXTVERSION, LINEERR_OPERATIONFAILED, LINEERR_NODRIVER, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM.




## -remarks



This function can be called before or after the device is opened by TAPI. If the device is currently open and has an extension version selected, the function gives that version number if it is within the requested range. If the selected version number is outside the requested range, the function returns LINEERR_INCOMPATIBLEEXTVERSION.




## -see-also




<a href="https://msdn.microsoft.com/ce978913-47a1-4387-bd1b-1795aaf82dd7">INITIALIZE_NEGOTIATION</a>



<a href="https://msdn.microsoft.com/d92fbf18-282d-485b-9d56-22e4896ece57">TSPI_lineNegotiateTSPIVersion</a>
 

 

