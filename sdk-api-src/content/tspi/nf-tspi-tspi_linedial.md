---
UID: NF:tspi.TSPI_lineDial
title: TSPI_lineDial function
author: windows-sdk-content
description: The TSPI_lineDial function dials the specified dialable number on the specified call.
old-location: tspi\tspi_linedial.htm
tech.root: tapi
ms.assetid: 8b24b9a3-af97-45dc-aaaf-d95ce9007ba8
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: TSPI_lineDial, TSPI_lineDial function [TAPI 2.2], _tspi_tspi_linedial, tspi.tspi_linedial, tspi/TSPI_lineDial
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
 - TSPI_lineDial
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineDial function


## -description


The 
<b>TSPI_lineDial</b> function dials the specified dialable number on the specified call.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The service provider's handle to the call to be dialed. The call state of <i>hdCall</i> can be any state except <i>idle</i> and <i>disconnected</i>.


### -param lpszDestAddress

Pointer to a <b>null</b>-terminated Unicode string that specifies the destination to be dialed using the standard dialable number format.


### -param dwCountryCode

The country or region code of the destination. The implementation uses this to select the call progress protocols for the destination address. If a value of 0 is specified, a default call-progress protocol defined by the service provider is used. TAPI does not validate this parameter when this function is called.


## -returns



Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALADDRESS, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCOUNTRYCODE, LINEERR_DIALBILLING, LINEERR_INVALCALLSTATE, LINEERR_DIALQUIET, LINEERR_ADDRESSBLOCKED, LINEERR_DIALDIALTONE, LINEERR_NOMEM, LINEERR_DIALPROMPT, LINEERR_OPERATIONUNAVAIL.




## -remarks



The service provider returns LINEERR_INVALCALLSTATE if the current state of the call does not allow dialing.

The service provider carries out no dialing if it returns LINEERR_INVALADDRESS.

If the service provider returns LINEERR_DIALBILLING, LINEERR_DIALQUIET, LINEERR_DIALDIALTONE, or LINEERR_DIALPROMPT, it should perform none of the actions otherwise performed by 
<b>TSPI_lineDial</b> (for example, no partial dialing, and no going offhook). This is because the service provider should pre-scan the number for unsupported characters first.

<b>TSPI_lineDial</b> is used for dialing on an existing call appearance; for example, call handles returned from 
<a href="https://msdn.microsoft.com/9c3d6a7d-b0bf-4068-9d64-e0c715a8c011">TSPI_lineMakeCall</a> with <b>NULL</b> as the <i>lpszDestAddress</i> or ending in ';', call handles returned from 
<a href="https://msdn.microsoft.com/0cd95e53-62d5-4318-961a-1136646fd222">TSPI_lineSetupTransfer</a> or 
<a href="https://msdn.microsoft.com/71b9720b-54dc-44a7-9fad-38dcd9f57ab3">TSPI_lineSetupConference</a>. 
<b>TSPI_lineDial</b> can be invoked multiple times in the course of dialing in the case of multistage dialing, if the line's device capabilities permit it.

If the string pointed to by the <i>lpszDestAddress</i> parameter in the previous call to the 
<a href="https://msdn.microsoft.com/9c3d6a7d-b0bf-4068-9d64-e0c715a8c011">TSPI_lineMakeCall</a> or 
<b>TSPI_lineDial</b> function is terminated with a semicolon, an empty string in the current call to 
<b>TSPI_lineDial</b> indicates that dialing is complete.

Multiple addresses can be provided in a single dial string separated by CRLF. Service providers that provide inverse multiplexing can establish individual physical calls with each of the addresses, and return a single call handle to the aggregate of all calls to the application. All addresses would use the same country or region code.

Dialing is considered complete after the address has been accepted by the service provider, not after the call is finally connected. Service providers that provide inverse multiplexing may allow multiple addresses to be provided at once. The service provider must send 
<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a> messages to TAPI to inform it about the progress of the call.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/9c3d6a7d-b0bf-4068-9d64-e0c715a8c011">TSPI_lineMakeCall</a>
 

 

