---
UID: NF:tspi.TSPI_lineGetExtensionID
title: TSPI_lineGetExtensionID function
author: windows-sdk-content
description: The TSPI_lineGetExtensionID function returns the extension identifier that the service provider supports for the indicated line device.
old-location: tspi\tspi_linegetextensionid.htm
old-project: Tapi
ms.assetid: aaea0a6a-bf22-491f-b1bf-d2195fba6af5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: TSPI_lineGetExtensionID, TSPI_lineGetExtensionID function [TAPI 2.2], _tspi_tspi_linegetextensionid, tspi.tspi_linegetextensionid, tspi/TSPI_lineGetExtensionID
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
 - TSPI_lineGetExtensionID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_lineGetExtensionID function


## -description


The 
<b>TSPI_lineGetExtensionID</b> function returns the extension identifier that the service provider supports for the indicated line device.


## -parameters




### -param dwDeviceID

The line device to be queried.


### -param dwTSPIVersion

An interface version number that was already negotiated for this device using 
<a href="https://msdn.microsoft.com/d92fbf18-282d-485b-9d56-22e4896ece57">TSPI_lineNegotiateTSPIVersion</a>. This function operates according to the interface specification at this version level.


### -param lpExtensionID

A pointer to a structure of type 
<a href="https://msdn.microsoft.com/bf7d9ccc-3f80-4e54-bcc2-cc2fef1d24af">LINEEXTENSIONID</a>. If the service provider supports provider-specific extensions, it fills this structure with the extension identifier of these extensions. If the service provider does not support extensions, it fills this structure with all zeros. (Therefore, a valid extension identifier cannot consist of all zeros.)


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL.




## -remarks



This function is typically called by TAPI in response to an application calling the 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a> function. The result returned by the service provider should be appropriate for use in a subsequent call to 
<a href="https://msdn.microsoft.com/cd7cc421-3efb-4fe1-858c-4d894f4d9377">TSPI_lineNegotiateExtVersion</a>. An extension identifier of all zeros is not a legal extension identifier, because the all-zeros value is used to indicate that the service provider does not support extensions.




## -see-also




<a href="https://msdn.microsoft.com/cd7cc421-3efb-4fe1-858c-4d894f4d9377">TSPI_lineNegotiateExtVersion</a>



<a href="https://msdn.microsoft.com/d92fbf18-282d-485b-9d56-22e4896ece57">TSPI_lineNegotiateTSPIVersion</a>
 

 

