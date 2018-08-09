---
UID: NF:tspi.TSPI_lineSetDefaultMediaDetection
title: TSPI_lineSetDefaultMediaDetection function
author: windows-sdk-content
description: The TSPI_lineSetDefaultMediaDetection procedure tells the service provider the new set of media types to detect for the indicated line (replacing any previous set).
old-location: tspi\tspi_linesetdefaultmediadetection.htm
old-project: tapi
ms.assetid: 407fa545-6890-4a8c-b5a8-bddeacc46e18
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: TSPI_lineSetDefaultMediaDetection, TSPI_lineSetDefaultMediaDetection function [TAPI 2.2], _tspi_tspi_linesetdefaultmediadetection, tspi.tspi_linesetdefaultmediadetection, tspi/TSPI_lineSetDefaultMediaDetection
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
 - TSPI_lineSetDefaultMediaDetection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_lineSetDefaultMediaDetection function


## -description


The 
<b>TSPI_lineSetDefaultMediaDetection</b> procedure tells the service provider the new set of media types to detect for the indicated line (replacing any previous set). It also sets the initial set of media types that should be monitored for on subsequent calls (inbound or outbound) on this line.


## -parameters




### -param hdLine

The handle to the line to have media monitoring set.


### -param dwMediaModes

The media type(s) of interest to TAPI. This parameter uses one of the 
<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ constants</a>:


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALMEDIAMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_NODRIVER, LINEERR_OPERATIONUNAVAIL.




## -remarks



TAPI typically calls this function to update the set of detected media types for the line to the union of all modes selected by all outstanding lineOpens whenever a line is Opened or Closed at the TAPI level. A 
<a href="https://msdn.microsoft.com/7dd39866-0b3e-47be-8aa8-adfb66df6644">lineOpen</a> call attempt is rejected if media detection is rejected. A single call to this procedure is typically the result of a 
<b>lineOpen</b> call that does not specify the device identifier LINEMAPPER. The device identifier LINEMAPPER is never used at the TSPI level.

TAPI must compute the union of media types desired by all clients and pass the result to this function. The service provider uses the set passed to this function by TAPI. TAPI ensures that the <i>dwMediaModes</i> parameter has at least one bit set and that no reserved bits are set. The service provider must perform any further validity checks on the media types, such as checking whether any media types are indeed supported by the service provider. The union of all media types can be the value 0 if the applications that have the line open are all either monitors or not interested in handling incoming calls.

There is no directly corresponding function at the TAPI level. This procedure corresponds to the "request media types" implied for the specific line by the 
<a href="https://msdn.microsoft.com/7dd39866-0b3e-47be-8aa8-adfb66df6644">lineOpen</a> procedure when it is called with the specific device identifier (other than LINEMAPPER).




## -see-also




<a href="https://msdn.microsoft.com/e7bc5604-20eb-48d8-a857-df8962c6b2ae">LINECALLPARAMS</a>



<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ Constants</a>



<a href="https://msdn.microsoft.com/d1041620-609b-476b-bdb7-e1e0cebd74f1">TSPI_lineClose</a>
 

 

