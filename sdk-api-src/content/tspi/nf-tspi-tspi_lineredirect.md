---
UID: NF:tspi.TSPI_lineRedirect
title: TSPI_lineRedirect function
author: windows-sdk-content
description: The TSPI_lineRedirect function redirects the specified offering call to the specified destination address.
old-location: tspi\tspi_lineredirect.htm
tech.root: Tapi
ms.assetid: 835fce4a-69c4-4a7e-846f-f05df4a24b96
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TSPI_lineRedirect, TSPI_lineRedirect function [TAPI 2.2], _tspi_tspi_lineredirect, tspi.tspi_lineredirect, tspi/TSPI_lineRedirect
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
 - TSPI_lineRedirect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineRedirect function


## -description


The 
<b>TSPI_lineRedirect</b> function redirects the specified offering call to the specified destination address.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The handle to the call to be redirected. The call state of <i>hdCall</i> can be <i>offering</i>.


### -param lpszDestAddress

Pointer to a null-terminated Unicode string that specifies the destination address. This follows the standard link format.


### -param dwCountryCode

The country or region code of the party the call is redirected to. If a value of 0 is specified, a default is used by the implementation. This parameter is not validated by TAPI when this function is called.


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_NOMEM, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCOUNTRYCODE, LINEERR_OPERATIONFAILED, LINEERR_INVALADDRESS, LINEERR_RESOURCEUNAVAIL.




## -remarks



The service provider does not redirect the call if it returns LINEERR_INVALADDRESS.

When this function is invoked, the service provider deflects the offering call to another address without first answering the call. Call redirect differs from call forwarding in that call forwarding is performed by the switch without the involvement of the called station; redirection can be done on a call-by-call basis by a client application, for example driven by caller ID information. It differs from call transfer in that transferring a call requires that the call first be answered.

After a call is successfully redirected, the call typically transitions to <i>idle</i>. The service provider indicates the new state using a 
<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a> message.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/2690992b-b155-4ae9-816a-e5fafaffa033">TSPI_lineAccept</a>



<a href="https://msdn.microsoft.com/ac7ec102-d7ad-4e63-833e-3c798487d7b4">TSPI_lineDrop</a>



<a href="https://msdn.microsoft.com/6c5a668e-9a9a-4a7a-98e9-bd8ec4b819b2">TSPI_lineGetDevCaps</a>
 

 

