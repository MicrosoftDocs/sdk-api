---
UID: NF:tspi.TSPI_linePark
title: TSPI_linePark function
author: windows-sdk-content
description: The TSPI_linePark function parks the specified call according to the specified park mode.
old-location: tspi\tspi_linepark.htm
tech.root: tapi
ms.assetid: 6ff14bfc-ba48-4f70-b732-81c19dba92c5
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: TSPI_linePark, TSPI_linePark function [TAPI 2.2], _tspi_tspi_linepark, tspi.tspi_linepark, tspi/TSPI_linePark
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
 - TSPI_linePark
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_linePark function


## -description


The 
<b>TSPI_linePark</b> function parks the specified call according to the specified park mode.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The handle to the call to be parked. The call state of <i>hdCall</i> can be <i>connected</i>.


### -param dwParkMode

The park mode with which the call is to be parked, only one of the 
<a href="https://msdn.microsoft.com/4b182c16-9d58-4244-bc5a-05c393800948">LINEPARKMODE_ constants</a>.


### -param lpszDirAddress

A pointer to <b>null</b>-terminated Unicode string that indicates the address where the call is to be parked when using directed park. The address is in dialable address format. This parameter is ignored for nondirected park.


### -param lpNonDirAddress

A pointer to a structure of type 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>. For nondirected park, the address where the call is parked is returned in this structure. This parameter is ignored for directed park. Within the 
<b>VARSTRING</b> structure, <i>dwStringFormat</i> must be set to STRINGFORMAT_ASCII (an ASCII string buffer containing a <b>null</b>-terminated string), and the terminating <b>NULL</b> is accounted for in the <i>dwStringSize</i>. If the memory pointed to by the <i>lpNonDirAddress</i> parameter is not large enough for the requested address, the 
<b>TSPI_linePark</b> function returns LINEERR_STRUCTURETOOSMALL.


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_NOMEM, LINEERR_INVALPARKMODE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALADDRESS, LINEERR_RESOURCEUNAVAIL, LINEERR_STRUCTURETOOSMALL.




## -remarks



All members of the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure, except <b>dwTotalSize</b>, are filled in by the service provider. The <b>dwTotalSize</b> member is filled in by TAPI, and the service provider must not overwrite this value.

Under directed park, the client application (through TAPI) specifies the address at which it wants to park the call. Under nondirected park, the switch determines the address and provides this to TAPI. In either case, a parked call can be unparked by specifying this address.

The parked call typically enters the <i>idle</i> call state after it is successfully parked. The service provider reports the new state using a 
<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a> message. A subsequent 
<a href="https://msdn.microsoft.com/941a9715-533e-489c-87b0-27a04be1d80e">TSPI_lineUnpark</a> creates a new, distinct call handle, regardless of whether 
<a href="https://msdn.microsoft.com/86f5490c-8401-4235-8ddd-313794bd5bf1">TSPI_lineCloseCall</a> has destroyed the old handle.

Some switches can remind the user after a call has been parked for some long amount of time. The service provider reports this to TAPI as an <i>offering</i> call with a call reason set to <i>reminder</i> (if this is known).




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/4b182c16-9d58-4244-bc5a-05c393800948">LINEPARKMODE_ Constants</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/86f5490c-8401-4235-8ddd-313794bd5bf1">TSPI_lineCloseCall</a>



<a href="https://msdn.microsoft.com/941a9715-533e-489c-87b0-27a04be1d80e">TSPI_lineUnpark</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>
 

 

