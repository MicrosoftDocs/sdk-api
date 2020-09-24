---
UID: NF:webservices.WsWriteEndCData
title: WsWriteEndCData function (webservices.h)
description: Ends a CDATA section in the writer.
helpviewer_keywords: ["WsWriteEndCData","WsWriteEndCData function [Web Services for Windows]","webservices/WsWriteEndCData","wsw.wswriteendcdata"]
old-location: wsw\wswriteendcdata.htm
tech.root: wsw
ms.assetid: 7b8c27b8-4540-4d47-9622-904428233d30
ms.date: 12/05/2018
ms.keywords: WsWriteEndCData, WsWriteEndCData function [Web Services for Windows], webservices/WsWriteEndCData, wsw.wswriteendcdata
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsWriteEndCData
 - webservices/WsWriteEndCData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsWriteEndCData
---

# WsWriteEndCData function


## -description

Ends a CDATA section in the writer.
      If <b>WsWriteEndCData</b> is called without a prior call to <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartcdata">WsWriteStartCData</a>, this function returns <b>WS_E_INVALID_OPERATION</b>.
      (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

## -parameters

### -param writer [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object to which the end CDATA section is written.  The pointer must reference a valid <b>XML Writer</b> object.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

</td>
</tr>
</table>