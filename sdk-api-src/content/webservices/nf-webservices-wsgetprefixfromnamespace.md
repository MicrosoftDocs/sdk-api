---
UID: NF:webservices.WsGetPrefixFromNamespace
title: WsGetPrefixFromNamespace function (webservices.h)
description: This function returns the prefix to which a namespace is bound. There may be more than one prefix in scope and this function is free to return any one of them.
helpviewer_keywords: ["WsGetPrefixFromNamespace","WsGetPrefixFromNamespace function [Web Services for Windows]","webservices/WsGetPrefixFromNamespace","wsw.wsgetprefixfromnamespace"]
old-location: wsw\wsgetprefixfromnamespace.htm
tech.root: wsw
ms.assetid: 69f4138b-4831-41c9-b1ed-31143edcc402
ms.date: 12/05/2018
ms.keywords: WsGetPrefixFromNamespace, WsGetPrefixFromNamespace function [Web Services for Windows], webservices/WsGetPrefixFromNamespace, wsw.wsgetprefixfromnamespace
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
 - WsGetPrefixFromNamespace
 - webservices/WsGetPrefixFromNamespace
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
 - WsGetPrefixFromNamespace
---

# WsGetPrefixFromNamespace function


## -description

This function returns the prefix to which a namespace is bound.
      There may be more than one prefix in scope and this function is free to return any one of them.


<div class="alert"><b>Note</b>  Under no
        conditions should a caller depend upon or expect a particular prefix to be returned when there is
        more than one prefix that may be returned.
      </div>
<div> </div>


If the value of the <i>required</i> parameter is set to <b>TRUE</b> and the Namespace is not bound to any Prefix a <b>WS_E_INVALID_FORMAT</b> exception will be returned.
        (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.) If the <i>required</i> parameter is  <b>FALSE</b>, and the Namespace is not bound to any Prefix the <i>prefix</i> parameter is <b>NULL</b> and the function returns S_FALSE.
      

If <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartelement">WsWriteStartElement</a> is called but the element is not committed the Namespaces and Prefixes referenced by the element and any attributes on the element is not available to
        this function.

## -parameters

### -param writer [in]

A pointer to a Writer with the namespace to search.  This must be a valid <b>WS_XML_WRITER</b> object
                    returned by <a href="/windows/desktop/api/webservices/nf-webservices-wscreatewriter">WsCreateWriter</a> and   may not be <b>NULL</b>.

### -param ns [in]

The namespace to search for.

### -param required [in]

Indicates whether or not an error should be returned if a matching prefix is not found.

### -param prefix

A reference to a prefix bound to the namespace or <b>NULL</b> if the value of the <i>required</i> parameter is <b>FALSE</b> and a matching
          namespace is not found.
        <div class="alert"><b>Note</b>  The value returned is valid only until the writer advances.</div>
<div> </div>

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
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
</table>

## -remarks

For the namespace "http://www.w3.org/XML/1998/namespace" it will return the prefix "xml".
      

For the namespace "http://www.w3.org/2000/xmlns/" it will return the prefix "xmlns".
      

The prefix returned should not be modified, and is only valid until the writer advances.