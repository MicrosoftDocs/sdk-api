---
UID: NF:tapi.lineSetCallQualityOfService
title: lineSetCallQualityOfService function (tapi.h)
author: windows-sdk-content
description: The lineSetCallQualityOfService function allows the application to attempt to change the quality of service parameters (reserved capacity and performance guarantees) for an existing call.
old-location: tapi2\linesetcallqualityofservice.htm
tech.root: Tapi
ms.assetid: 6a977dab-70f6-4462-a94f-78acdec7decf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linesetcallqualityofservice, lineSetCallQualityOfService, lineSetCallQualityOfService function [TAPI 2.2], tapi/lineSetCallQualityOfService, tapi2.linesetcallqualityofservice"
ms.topic: function
req.header: tapi.h
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetCallQualityOfService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSetCallQualityOfService function


## -description


The 
<b>lineSetCallQualityOfService</b> function allows the application to attempt to change the quality of service parameters (reserved capacity and performance guarantees) for an existing call. Except for basic parameter validation, this is a straight pass-through to a service provider.


## -parameters




### -param hCall

Handle to the call. The application must have OWNER privilege.


### -param lpSendingFlowspec

Pointer to memory containing a 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure followed by provider-specific data. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory in the application process, because TAPI will not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the service provider.


### -param dwSendingFlowspecSize

Total size of the <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure and accompanying provider-specific data, in bytes. This is equivalent to what would have been stored in <b>SendingFlowspec</b> in a 
<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure. 


### -param lpReceivingFlowspec

Pointer to memory containing a <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure followed by provider-specific data. The provider-specific portion following the <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure must not contain pointers to other blocks of memory in the application process, because TAPI will not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the service provider.


### -param dwReceivingFlowspecSize

Total size of the <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> and accompanying provider-specific data, in bytes. This is equivalent to what would have been stored in <b>ReceivingFlowspec</b> in a <a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure. 


## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALCALLHANDLE, LINEERR_INVALCALLSTATE, LINEERR_INVALPARAM, LINEERR_INVALPOINTER, LINEERR_INVALRATE, LINEERR_NOMEM, LINEERR_NOTOWNER, LINEERR_OPERATIONUNAVAIL, LINEERR_OPERATIONFAILED, LINEERR_RATEUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

