---
UID: NF:tapi.lineProxyResponse
title: lineProxyResponse function (tapi.h)
description: Indicates completion of a proxy request by a registered proxy handler, such as an ACD agent handler on a server.
helpviewer_keywords: ["_tapi2_lineproxyresponse","lineProxyResponse","lineProxyResponse function [TAPI 2.2]","tapi/lineProxyResponse","tapi2.lineproxyresponse"]
old-location: tapi2\lineproxyresponse.htm
tech.root: tapi3
ms.assetid: af774fc5-d013-4da2-a737-9e99c09456a0
ms.date: 12/05/2018
ms.keywords: _tapi2_lineproxyresponse, lineProxyResponse, lineProxyResponse function [TAPI 2.2], tapi/lineProxyResponse, tapi2.lineproxyresponse
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineProxyResponse
 - tapi/lineProxyResponse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineProxyResponse
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
<a href="/windows/desktop/Tapi/line-proxyrequest">LINE_PROXYREQUEST</a> message. In the case of proxy requests that return data to the client application, the proxy handler should have filled in the necessary structure in this buffer before calling this function. The <b>dwNeededSize</b> and <b>dwUsedSize</b> members of the structure to be returned must have been set appropriately. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are incorrect, it is possible that data could be overwritten. For more information about setting structure sizes, see 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a>.</div>
<div> </div>

### -param dwResult

A function result returned to the calling application in a 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message (generated automatically by TAPI). Must be zero or one of the negative error values defined for the called function.

## -returns

Returns zero if the function succeeds or one of these negative error values:

<b>LINEERR_INVALLINEHANDLE</b>, <b>LINEERR_INVALPARAM</b>, <b>LINEERR_INVALPOINTER</b>, <b>LINEERR_NOMEM</b>, <b>LINEERR_NOTREGISTERED</b>, <b>LINEERR_OPERATIONFAILED</b>, <b>LINE ERR_OPERATIONUNAVAIL</b>, <b>LINEERR_RESOURCEUNAVAIL</b>, <b>LINEERR_UNINITIALIZED</b>.

## -see-also

<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>