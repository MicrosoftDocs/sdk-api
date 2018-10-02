---
UID: NF:tapi.lineUncompleteCall
title: lineUncompleteCall function
author: windows-sdk-content
description: The lineUncompleteCall function cancels the specified call completion request on the specified line.
old-location: tapi2\lineuncompletecall.htm
tech.root: TAPI
ms.assetid: e6b87d84-071c-4b75-afbf-569a5a861e3a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: "_tapi2_lineuncompletecall, lineUncompleteCall, lineUncompleteCall function [TAPI 2.2], tapi/lineUncompleteCall, tapi2.lineuncompletecall"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - lineUncompleteCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineUncompleteCall function


## -description


The 
<b>lineUncompleteCall</b> function cancels the specified call completion request on the specified line.


## -parameters




### -param hLine

Handle to the line device on which a call completion is to be canceled.


### -param dwCompletionID

Completion identifier for the request that is to be canceled.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCOMPLETIONID, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_OPERATIONUNAVAIL.




## -see-also




<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

