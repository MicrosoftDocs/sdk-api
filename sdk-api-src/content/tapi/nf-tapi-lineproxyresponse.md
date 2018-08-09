---
UID: NF:tapi.lineProxyResponse
title: lineProxyResponse function
author: windows-sdk-content
description: Indicates completion of a proxy request by a registered proxy handler, such as an ACD agent handler on a server.
old-location: tapi2\lineproxyresponse.htm
old-project: tapi
ms.assetid: af774fc5-d013-4da2-a737-9e99c09456a0
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_lineproxyresponse, lineProxyResponse, lineProxyResponse function [TAPI 2.2], tapi/lineProxyResponse, tapi2.lineproxyresponse"
ms.prod: windows
ms.technology: windows-sdk
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
 - lineProxyResponse
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineProxyResponse function


## -description


The 
<b>lineProxyResponse</b> function indicates completion of a proxy request by a registered proxy handler, such as an ACD agent handler on a server.


## -parameters




### -param hLine

A handle to the open line device.


### -param lpProxyRequest

A pointer to the proxy request buffer given to the application by TAPI in a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message. In the case of proxy requests that return data to the client application, the proxy handler should have filled in the necessary structure in this buffer before calling this function. The <b>dwNeededSize</b> and <b>dwUsedSize</b> members of the structure to be returned must have been set appropriately. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are incorrect, it is possible that data could be overwritten. For more information about setting structure sizes, see 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a>.</div>
<div> </div>

### -param dwResult

A function result returned to the calling application in a 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message (generated automatically by TAPI). Must be zero or one of the negative error values defined for the called function.


## -returns



Returns zero if the function succeeds or one of these negative error values:

<b>LINEERR_INVALLINEHANDLE</b>, <b>LINEERR_INVALPARAM</b>, <b>LINEERR_INVALPOINTER</b>, <b>LINEERR_NOMEM</b>, <b>LINEERR_NOTREGISTERED</b>, <b>LINEERR_OPERATIONFAILED</b>, <b>LINE ERR_OPERATIONUNAVAIL</b>, <b>LINEERR_RESOURCEUNAVAIL</b>, <b>LINEERR_UNINITIALIZED</b>.




## -see-also




<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

