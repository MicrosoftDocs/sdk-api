---
UID: NF:tspi.TSPI_phoneGetDevCaps
title: TSPI_phoneGetDevCaps function
author: windows-sdk-content
description: The TSPI_phoneGetDevCaps function queries a specified phone device to determine its telephony capabilities.
old-location: tspi\tspi_phonegetdevcaps.htm
tech.root: tapi
ms.assetid: d929ed39-ba1d-4eae-9667-86d904ba96a8
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: TSPI_phoneGetDevCaps, TSPI_phoneGetDevCaps function [TAPI 2.2], _tspi_tspi_phonegetdevcaps, tspi.tspi_phonegetdevcaps, tspi/TSPI_phoneGetDevCaps
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
 - TSPI_phoneGetDevCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_phoneGetDevCaps function


## -description


The 
<b>TSPI_phoneGetDevCaps</b> function queries a specified phone device to determine its telephony capabilities.


## -parameters




### -param dwDeviceID

The phone device to be queried.


### -param dwTSPIVersion

The negotiated TSPI version number. This value is negotiated for this device through the 
<a href="https://msdn.microsoft.com/a6bca1a3-a6cd-4cb5-80e9-0da0ad6ba8dc">TSPI_phoneNegotiateTSPIVersion</a> function.


### -param dwExtVersion

The negotiated extension version number. This value is negotiated for this device through the 
<a href="https://msdn.microsoft.com/03ea6d25-8e65-4c8a-80dc-f2ecd214ad0e">TSPI_phoneNegotiateExtVersion</a> function.


### -param lpPhoneCaps

A pointer to memory into which the service provider writes a variably sized structure of type 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>. Upon successful completion of the request, this structure is filled with phone device capability information. Prior to calling 
<b>TSPI_phoneGetDevCaps</b>, the application sets the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INCOMPATIBLEEXTVERSION, PHONEERR_OPERATIONFAILED, PHONEERR_NODRIVER, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.




## -remarks



The service provider fills in all the members of the 
<a href="https://msdn.microsoft.com/f8316587-f279-419a-a35d-194df3fc8383">PHONEBUTTONINFO</a> data structure, except for <b>dwTotalSize</b>, which is filled in by TAPI. The service provider must not overwrite the <b>dwTotalSize</b> member.

If <i>dwExtVersion</i> is zero, no extension information is requested. If it is nonzero, it holds a value that has already been negotiated for this device with the 
<a href="https://msdn.microsoft.com/03ea6d25-8e65-4c8a-80dc-f2ecd214ad0e">TSPI_phoneNegotiateExtVersion</a> function. The service provider fills in device- and vendor-specific extended information according to the extension version specified.

After the service provider returns from the 
<b>TSPI_phoneGetDevCaps</b> function, TAPI sets the <b>dwPhoneStates</b> member of the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure as follows:

<pre class="syntax" xml:space="preserve"><code>PHONECAPS.dwPhoneStates |=
    PHONESTATE_OWNER |
    PHONESTATE_MONITORS |
    PHONESTATE_REINIT;</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/f8316587-f279-419a-a35d-194df3fc8383">PHONEBUTTONINFO</a>



<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/03ea6d25-8e65-4c8a-80dc-f2ecd214ad0e">TSPI_phoneNegotiateExtVersion</a>
 

 

