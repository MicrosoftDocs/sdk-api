---
UID: NF:tspi.TSPI_providerShutdown
title: TSPI_providerShutdown function
author: windows-sdk-content
description: The TSPI_providerShutdown function shuts down the service provider. The service provider terminates any activities it has in progress and releases any resources it has allocated.
old-location: tspi\tspi_providershutdown.htm
tech.root: tapi
ms.assetid: b13e0ed6-c053-4290-bc4c-5f66e4a376b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TSPI_providerShutdown, TSPI_providerShutdown function [TAPI 2.2], _tspi_tspi_providershutdown, tspi.tspi_providershutdown, tspi/TSPI_providerShutdown
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
 - TSPI_providerShutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_providerShutdown function


## -description


The 
<b>TSPI_providerShutdown</b> function shuts down the service provider. The service provider terminates any activities it has in progress and releases any resources it has allocated.


## -parameters




### -param dwTSPIVersion

The version of the TSPI definition under which this function must operate. The caller can use 
<a href="https://msdn.microsoft.com/d92fbf18-282d-485b-9d56-22e4896ece57">TSPI_lineNegotiateTSPIVersion</a> or 
<a href="https://msdn.microsoft.com/a6bca1a3-a6cd-4cb5-80e9-0da0ad6ba8dc">TSPI_phoneNegotiateTSPIVersion</a> with the special <i>dwDeviceID</i>
<a href="https://msdn.microsoft.com/ce978913-47a1-4387-bd1b-1795aaf82dd7">INITIALIZE_NEGOTIATION</a> to negotiate a version that is guaranteed to be acceptable to the service provider.


### -param dwPermanentProviderID

This parameter allows the service provider to determine which among multiple possible instances of the service provider is being shut down. The value of the parameter is identical to that passed in the parameter of the same name in 
<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a>.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_NOMEM.




## -remarks



The final paired call to this function must be the last call to any of the TSPI functions prefixed with <b>TSPI_line</b> or <b>TSPI_phone</b> other than 
<a href="https://msdn.microsoft.com/d92fbf18-282d-485b-9d56-22e4896ece57">TSPI_lineNegotiateTSPIVersion</a>, or 
<a href="https://msdn.microsoft.com/a6bca1a3-a6cd-4cb5-80e9-0da0ad6ba8dc">TSPI_phoneNegotiateTSPIVersion</a>. It is the caller's responsibility to ensure this.

This function should always succeed except in extraordinary circumstances. Most callers will probably ignore the return code because they will be unable to compensate for any error that occurs. The specified return values are more advisory for development diagnostic purposes than anything else.

There is no directly corresponding function in TAPI. In TAPI, multiple different usage instances can be outstanding, with an "application handle" parameter to identify the instance to be operated on. In TSPI, the interface architecture supports only a single usage instance for each distinct service provider.




## -see-also




<a href="https://msdn.microsoft.com/d92fbf18-282d-485b-9d56-22e4896ece57">TSPI_lineNegotiateTSPIVersion</a>



<a href="https://msdn.microsoft.com/a6bca1a3-a6cd-4cb5-80e9-0da0ad6ba8dc">TSPI_phoneNegotiateTSPIVersion</a>



<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a>
 

 

