---
UID: NF:webservices.WsWriteQualifiedName
title: WsWriteQualifiedName function (webservices.h)
description: Writes an XML qualified name to the Writer.
helpviewer_keywords: ["WsWriteQualifiedName","WsWriteQualifiedName function [Web Services for Windows]","webservices/WsWriteQualifiedName","wsw.wswritequalifiedname"]
old-location: wsw\wswritequalifiedname.htm
tech.root: wsw
ms.assetid: 1e0f6419-ef76-4465-bd1d-a92f4bf11903
ms.date: 12/05/2018
ms.keywords: WsWriteQualifiedName, WsWriteQualifiedName function [Web Services for Windows], webservices/WsWriteQualifiedName, wsw.wswritequalifiedname
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
 - WsWriteQualifiedName
 - webservices/WsWriteQualifiedName
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
 - WsWriteQualifiedName
---

# WsWriteQualifiedName function


## -description

Writes an XML qualified name to the Writer.

## -parameters

### -param writer [in]

A pointer to the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object to which the qualified name is written.  The pointer must reference a valid <b>XML Writer</b> object.

### -param prefix [in, optional]

A WS_XML_STRING pointer to the prefix used by the qualified name.  If the value referenced by this parameter is <b>NULL</b> the Writer will choose a prefix.

### -param localName [in]

A WS_XML_STRING pointer to the local name used by the qualified name.  It must be at least one character long.

### -param ns [in, optional]

A WS_XML_STRING pointer to the namespace used for the qualified name.
        
If no prefix is specified the Writer may use a prefix in scope that is bound to the specified namespace or it may generate a prefix and include an XMLNS attribute.

If a prefix is specified the Writer uses that prefix and may include an XMLNS attribute if needed to override an existing prefix in scope.

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
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
</table>

## -remarks

<ul>
<li>If the prefix is <b>NULL</b>, then the namespace must not be <b>NULL</b>.  In this case the writer will try to find a prefix in scope that is bound to the specified namespace.  If an appropriate prefix is found it will be used.  If not the Writer will generate a prefix and insert an XMLNS attribute on the current element.  If the writer is not in an element, then the function will return <b>WS_E_INVALID_FORMAT</b>.

(See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)</li>
<li>If the prefix is not <b>NULL</b> and the namespace is not <b>NULL</b> the Writer will verify that the prefix is currently bound to the specified namespace and will return <b>WS_E_INVALID_FORMAT</b> if not.
</li>
<li>If the prefix is not <b>NULL</b> and the namespace is <b>NULL</b> the Writer will use the prefix and local name to write the qualified name.
</li>
</ul>