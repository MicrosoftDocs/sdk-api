---
UID: NF:tspi.TSPI_lineNegotiateTSPIVersion
title: TSPI_lineNegotiateTSPIVersion function
author: windows-sdk-content
description: The TSPI_lineNegotiateTSPIVersion function returns the highest SPI version the service provider can operate under for this device, given the range of possible SPI versions.
old-location: tspi\tspi_linenegotiatetspiversion.htm
tech.root: tapi
ms.assetid: d92fbf18-282d-485b-9d56-22e4896ece57
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: TSPI_lineNegotiateTSPIVersion, TSPI_lineNegotiateTSPIVersion function [TAPI 2.2], _tspi_tspi_linenegotiatetspiversion, tspi.tspi_linenegotiatetspiversion, tspi/TSPI_lineNegotiateTSPIVersion
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
 - TSPI_lineNegotiateTSPIVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineNegotiateTSPIVersion function


## -description


The 
<b>TSPI_lineNegotiateTSPIVersion</b> function returns the highest SPI version the service provider can operate under for this device, given the range of possible SPI versions.


## -parameters




### -param dwDeviceID

Identifies the line device for which interface version negotiation is to be performed. In addition to device identifiers within the range the service provider supports, this may be the value: 







#### INITIALIZE_NEGOTIATION

This value is used to signify that an overall interface version is to be negotiated.


### -param dwLowVersion

The lowest TSPI version number under which TAPI can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number.


### -param dwHighVersion

The highest TSPI version number under which TAPI can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number.


### -param lpdwTSPIVersion

A pointer to a <b>DWORD</b>. The service provider fills this location with the highest TSPI version number, within the range requested by the caller, under which the service provider can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number. If the requested range does not overlap the range supported by the service provider, the function returns LINEERR_INCOMPATIBLEAPIVERSION.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_OPERATIONUNAVAIL, LINEERR_NODRIVER, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.




## -remarks



When <i>dwDeviceID</i> is 
<a href="https://msdn.microsoft.com/ce978913-47a1-4387-bd1b-1795aaf82dd7">INITIALIZE_NEGOTIATION</a>, this function must not return LINEERR_OPERATIONUNAVAIL, because this function (with that value) is mandatory for negotiating the overall interface version even if the service provider supports no line devices.




## -see-also




<a href="https://msdn.microsoft.com/ce978913-47a1-4387-bd1b-1795aaf82dd7">INITIALIZE_NEGOTIATION</a>



<a href="https://msdn.microsoft.com/994fad0e-5958-4d93-8952-9db2bbe01f44">TSPI Versioning</a>



<a href="https://msdn.microsoft.com/aaea0a6a-bf22-491f-b1bf-d2195fba6af5">TSPI_lineGetExtensionID</a>



<a href="https://msdn.microsoft.com/cd7cc421-3efb-4fe1-858c-4d894f4d9377">TSPI_lineNegotiateExtVersion</a>



<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a>
 

 

