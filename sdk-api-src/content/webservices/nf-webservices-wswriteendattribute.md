---
UID: NF:webservices.WsWriteEndAttribute
title: WsWriteEndAttribute function (webservices.h)
description: This operation finishes writing an attribute to the current element. If WsWriteStartAttribute is called the Writer does not permit another element or attribute to be written until WsWriteEndAttribute is called.
helpviewer_keywords: ["WsWriteEndAttribute","WsWriteEndAttribute function [Web Services for Windows]","webservices/WsWriteEndAttribute","wsw.wswriteendattribute"]
old-location: wsw\wswriteendattribute.htm
tech.root: wsw
ms.assetid: 8747c484-19b3-46b2-beee-80b220011def
ms.date: 12/05/2018
ms.keywords: WsWriteEndAttribute, WsWriteEndAttribute function [Web Services for Windows], webservices/WsWriteEndAttribute, wsw.wswriteendattribute
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
 - WsWriteEndAttribute
 - webservices/WsWriteEndAttribute
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
 - WsWriteEndAttribute
---

# WsWriteEndAttribute function


## -description

This operation finishes writing an attribute to the current element.
      If <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartattribute">WsWriteStartAttribute</a> is called the Writer does not permit another element
        or attribute to be written until <b>WsWriteEndAttribute</b> is called.

## -parameters

### -param writer [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object to which the attribute is written.  The pointer must reference a valid <b>XML Writer</b> object.

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