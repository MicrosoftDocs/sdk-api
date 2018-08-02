---
UID: NF:tspi.TSPI_lineUnpark
title: TSPI_lineUnpark function
author: windows-sdk-content
description: The TSPI_lineUnpark function retrieves the call parked at the specified address and returns a call handle for it.
old-location: tspi\tspi_lineunpark.htm
old-project: Tapi
ms.assetid: 941a9715-533e-489c-87b0-27a04be1d80e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: TSPI_lineUnpark, TSPI_lineUnpark function [TAPI 2.2], _tspi_tspi_lineunpark, tspi.tspi_lineunpark, tspi/TSPI_lineUnpark
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
 - TSPI_lineUnpark
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_lineUnpark function


## -description


The 
<b>TSPI_lineUnpark</b> function retrieves the call parked at the specified address and returns a call handle for it.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdLine

The handle to the line on which a call is to be unparked.


### -param dwAddressID

The address on <i>hdLine</i> at which to originate the unpark. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades. TAPI does not validate this parameter when this function is called.


### -param htCall

The TAPI handle to the new unparked call. The service provider must save this and use it in all subsequent calls to the 
<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">LINEEVENT</a> procedure reporting events on the call.


### -param lphdCall

A pointer to an 
<a href="https://msdn.microsoft.com/8bb1c3fe-a3de-4299-bc15-58321c5da549">HDRVCALL</a> representing the service provider's identifier for the new unparked call. The service provider must fill this location with its handle for the call before this procedure returns. This handle is invalid if the function results in an error.


### -param lpszDestAddress

A pointer to a null-terminated Unicode string that contains the address where the call is parked. The address is in dialable address format.


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_NOMEM, LINEERR_INVALPOINTER, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_INVALADDRESS, LINEERR_RESOURCEUNAVAIL.




## -remarks



This function differs from the corresponding TAPI function in that it follows the TSPI model for beginning the lifetime of a call. TAPI and the service provider exchange opaque handles representing the call with one another. In addition, the service provider is permitted to do callbacks for the new call before it returns from this procedure. In any case, the service provider must also treat the handle it returned as "not yet valid" until after the matching 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> message reports success. In other words, it must not issue any 
<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">LINEEVENT</a> messages for the new call or include it in call counts in messages or status data structures for the line.

The call handle created by this function is a new, distinct, call handle even if an original call handle for the call is still in existence (it has not been destroyed by 
<a href="https://msdn.microsoft.com/86f5490c-8401-4235-8ddd-313794bd5bf1">TSPI_lineCloseCall</a>).




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/86f5490c-8401-4235-8ddd-313794bd5bf1">TSPI_lineCloseCall</a>



<a href="https://msdn.microsoft.com/6ff14bfc-ba48-4f70-b732-81c19dba92c5">TSPI_linePark</a>
 

 

