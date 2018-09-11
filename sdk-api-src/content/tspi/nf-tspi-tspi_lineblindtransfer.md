---
UID: NF:tspi.TSPI_lineBlindTransfer
title: TSPI_lineBlindTransfer function
author: windows-sdk-content
description: The TSPI_lineBlindTransfer function performs a blind or single-step transfer of the specified call to the specified destination address.
old-location: tspi\tspi_lineblindtransfer.htm
tech.root: tapi
ms.assetid: 825f132c-fb0e-4e3d-bd2c-4e5226a30ba3
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: TSPI_lineBlindTransfer, TSPI_lineBlindTransfer function [TAPI 2.2], _tspi_tspi_lineblindtransfer, tspi.tspi_lineblindtransfer, tspi/TSPI_lineBlindTransfer
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
 - TSPI_lineBlindTransfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineBlindTransfer function


## -description


The 
<b>TSPI_lineBlindTransfer</b> function performs a blind or single-step transfer of the specified call to the specified destination address.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The service provider's handle to the call to be transferred. The call state of <i>hdCall</i> can be <i>connected</i>.


### -param lpszDestAddress

A pointer to a null-terminated Unicode string identifying where the call is to be transferred to. The destination address uses the standard dialable number format.


### -param dwCountryCode

The country or region code of the destination. The implementation should use this to select the call progress protocols for the destination address. If a value of 0 is specified, the service provider should use a default. TAPI does not validate <i>dwCountryCode</i> when this function is called.


## -returns



Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_NOMEM, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESS, LINEERR_OPERATIONFAILED, LINEERR_ADDRESSBLOCKED, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCOUNTRYCODE.




## -remarks



The service provider carries out no dialing if it returns LINEERR_INVALADDRESS.

Blind transfer differs from a consultation transfer in that no consultation call is made visible to TAPI. Typically, after the blind transfer successfully completes, the specified call is cleared from the line it was on and transitions to the <i>idle</i> state. The service provider's call handle must remain valid after the transfer has completed. TAPI causes this handle to be invalidated when it is no longer interested in the transferred call using 
<a href="https://msdn.microsoft.com/86f5490c-8401-4235-8ddd-313794bd5bf1">TSPI_lineCloseCall</a>.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/86f5490c-8401-4235-8ddd-313794bd5bf1">TSPI_lineCloseCall</a>
 

 

