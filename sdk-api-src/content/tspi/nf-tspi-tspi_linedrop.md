---
UID: NF:tspi.TSPI_lineDrop
title: TSPI_lineDrop function
author: windows-sdk-content
description: The TSPI_lineDrop function drops or disconnects the specified call.
old-location: tspi\tspi_linedrop.htm
tech.root: tapi
ms.assetid: ac7ec102-d7ad-4e63-833e-3c798487d7b4
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: TSPI_lineDrop, TSPI_lineDrop function [TAPI 2.2], _tspi_tspi_linedrop, tspi.tspi_linedrop, tspi/TSPI_lineDrop
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
 - TSPI_lineDrop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineDrop function


## -description


The 
<b>TSPI_lineDrop</b> function drops or disconnects the specified call. User-user information can optionally be transmitted as part of the call disconnect. This function can be called by the application at any time. When 
<b>TSPI_lineDrop</b> returns, the call should be <i>idle</i>.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The service provider's handle to the call to be dropped. The call state of <i>hdCall</i> can be any state except <i>idle</i>.


### -param lpsUserUserInfo

This pointer is only valid if <b>dwSize</b> is nonzero. It specifies a pointer to a <b>null</b>-terminated string containing user-user information to be sent to the remote party as part of the call disconnect. This pointer is <b>NULL</b> if no user-user information is to be sent. User-user information is only sent if supported by the underlying network (see 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>).


### -param dwSize

The size in bytes of the user-user information in <i>lpsUserUserInfo</i>. If <i>lpsUserUserInfo</i> is <b>NULL</b>, <i>dwSize</i> is ignored.


## -returns



Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG, LINEERR_OPERATIONUNAVAIL.




## -remarks



The service provider returns LINEERR_INVALCALLSTATE if the current state of the call does not allow the call to be dropped.

When invoking 
<b>TSPI_lineDrop</b>, related calls can sometimes be affected as well. For example, dropping a conference call may drop all individual participating calls. 
<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a> messages are sent to TAPI for all calls whose call state is affected. Typically, a dropped call transitions to the <i>idle</i> state. Invoking 
<b>TSPI_lineDrop</b> on a call in the <i>offering</i> state rejects the call. Not all telephone networks provide this capability.

In situations where the call to be dropped is a consultation call established during transfer or conference call establishment, the original call that was placed in the <i>OnHoldPending</i> state is reconnected to and it typically re-enters the <i>connected</i> call state.

TAPI has the option to send user-user information at the time of the drop. Even if user-user information can be sent, there is no guarantee that the network will deliver this information to the remote party.

<div class="alert"><b>Note</b>  In various bridged or party line configurations when multiple parties are on the call, 
<b>TSPI_lineDrop</b> may not actually clear the call.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/6c5a668e-9a9a-4a7a-98e9-bd8ec4b819b2">TSPI_lineGetDevCaps</a>
 

 

