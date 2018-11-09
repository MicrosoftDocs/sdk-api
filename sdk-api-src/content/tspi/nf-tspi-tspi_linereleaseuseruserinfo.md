---
UID: NF:tspi.TSPI_lineReleaseUserUserInfo
title: TSPI_lineReleaseUserUserInfo function
author: windows-sdk-content
description: The TSPI_lineReleaseUserUserInfo function informs the service provider that the user-user information contained in the LINECALLINFO structure has been processed, and that subsequently received user-user information can now be written into that structure.
old-location: tspi\tspi_linereleaseuseruserinfo.htm
tech.root: tapi
ms.assetid: 3c760254-a8c0-406a-aa15-3a5a42aba2e7
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: TSPI_lineReleaseUserUserInfo, TSPI_lineReleaseUserUserInfo function [TAPI 2.2], _tspi_tspi_linereleaseuseruserinfo, tspi.tspi_linereleaseuseruserinfo, tspi/TSPI_lineReleaseUserUserInfo
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
 - TSPI_lineReleaseUserUserInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineReleaseUserUserInfo function


## -description


The 
<b>TSPI_lineReleaseUserUserInfo</b> function informs the service provider that the user-user information contained in the 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure has been processed, and that subsequently received user-user information can now be written into that structure. The service provider sends a 
<a href="https://msdn.microsoft.com/74d16c8c-ef58-41a0-b777-225ee601ee6c">LINE_CALLINFO</a> message indicating LINECALLINFOSTATE_USERUSERINFO when new information is available.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The service provider's handle to the call for which user-user information is to be released. The call state of <i>hdCall</i> can be <i>any</i>.


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.




## -remarks



The 
<b>TSPI_lineReleaseUserUserInfo</b> function permits control of the flow of incoming user-user information on an ISDN connection. When a new, complete user-user information message is received, the service provider informs TAPI using a 
<a href="https://msdn.microsoft.com/74d16c8c-ef58-41a0-b777-225ee601ee6c">LINE_CALLINFO</a> message (specifying LINECALLINFOSTATE_USERUSERINFO). The user-user information and other fields in 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> can be examined by multiple calls to 
<a href="https://msdn.microsoft.com/9ef43928-05aa-4ec6-bc44-f07a63d8ecdf">TSPI_lineGetCallInfo</a>. The service provider must not overwrite previous user-user information in 
<b>LINECALLINFO</b> with newer information until after 
<b>TSPI_lineReleaseUserUserInfo</b> has been called. The service provider must buffer subsequently received user-user information until the previous information is released. Any remaining buffered information can be discarded when 
<a href="https://msdn.microsoft.com/86f5490c-8401-4235-8ddd-313794bd5bf1">TSPI_lineCloseCall</a> is invoked.

If this function is invoked while there is no user-user information in 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>, the service provider should nevertheless return an indication of success.

For backward compatibility, TAPI automatically returns LINEERR_OPERATIONUNAVAIL if this function is invoked for a call on a line under the control of a service provider that does not export the function.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/74d16c8c-ef58-41a0-b777-225ee601ee6c">LINE_CALLINFO</a>



<a href="https://msdn.microsoft.com/9ef43928-05aa-4ec6-bc44-f07a63d8ecdf">TSPI_lineGetCallInfo</a>
 

 

