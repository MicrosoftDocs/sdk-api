---
UID: NF:tapi.lineGetProxyStatus
title: lineGetProxyStatus function
author: windows-sdk-content
description: The lineGetProxyStatus function returns a list of proxy request types that are currently being serviced for the specified device.
old-location: tapi2\linegetproxystatus.htm
old-project: tapi
ms.assetid: 0684f52f-13dd-4734-9242-acd03f7a25ae
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_linegetproxystatus, lineGetProxyStatus, lineGetProxyStatus function [TAPI 2.2], tapi/lineGetProxyStatus, tapi2.linegetproxystatus"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
req.include-header: 
req.redist: 
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
req.typenames: FLICK_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGetProxyStatus
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineGetProxyStatus function


## -description


The 
<b>lineGetProxyStatus</b> function returns a list of proxy request types that are currently being serviced for the specified device.


## -parameters




### -param hLineApp

Handle to the application's registration with TAPI.


### -param dwDeviceID

Line device to be queried.


### -param dwAppAPIVersion

Version number of TAPI to be used.


### -param lpLineProxyReqestList

TBD




#### - lpLineProxyRequestList

Pointer to a variably sized structure of type 
<a href="https://msdn.microsoft.com/dc417954-56b4-4436-9582-7b656121fd6f">LINEPROXYREQUESTLIST</a>. Upon successful completion of the request, this structure is filled with a list of the currently supported proxy requests. Prior to calling 
<b>lineGetProxyStatus</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic.</div>
<div> </div>

## -returns



Returns zero if the request succeeds; otherwise, the function returns one of the following negative error values:

LINEERR_BADDEVICEID, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/dc417954-56b4-4436-9582-7b656121fd6f">LINEPROXYREQUESTLIST</a>
 

 

