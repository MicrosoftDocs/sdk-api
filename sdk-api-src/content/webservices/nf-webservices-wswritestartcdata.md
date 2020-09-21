---
UID: NF:webservices.WsWriteStartCData
title: WsWriteStartCData function (webservices.h)
description: This operation starts a CDATA section in the writer.
helpviewer_keywords: ["WsWriteStartCData","WsWriteStartCData function [Web Services for Windows]","webservices/WsWriteStartCData","wsw.wswritestartcdata"]
old-location: wsw\wswritestartcdata.htm
tech.root: wsw
ms.assetid: c233244c-24b6-4baa-ba36-697283ff33f3
ms.date: 12/05/2018
ms.keywords: WsWriteStartCData, WsWriteStartCData function [Web Services for Windows], webservices/WsWriteStartCData, wsw.wswritestartcdata
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
 - WsWriteStartCData
 - webservices/WsWriteStartCData
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
 - WsWriteStartCData
---

# WsWriteStartCData function


## -description

This operation starts a CDATA section in the writer.
      CDATA sections cannot be nested and cannot appear at the root of the document.  <div class="alert"><b>Note</b>  Some encodings do not support CDATA
        and will generate text instead.
      </div>
<div> </div>The CDATA section is completed by calling <a href="/windows/desktop/api/webservices/nf-webservices-wswriteendcdata">WsWriteEndCData</a>.

## -parameters

### -param writer [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object to which the CDATA section is written.  The pointer must reference a valid <b>XML Writer</b> object.

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