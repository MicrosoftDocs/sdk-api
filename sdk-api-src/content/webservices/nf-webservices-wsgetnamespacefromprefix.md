---
UID: NF:webservices.WsGetNamespaceFromPrefix
title: WsGetNamespaceFromPrefix function (webservices.h)
description: This function returns a namespace from the prefix to which it is bound.
helpviewer_keywords: ["WsGetNamespaceFromPrefix","WsGetNamespaceFromPrefix function [Web Services for Windows]","webservices/WsGetNamespaceFromPrefix","wsw.wsgetnamespacefromprefix"]
old-location: wsw\wsgetnamespacefromprefix.htm
tech.root: wsw
ms.assetid: 35351ce3-4ff9-4a15-856b-c3ee485f9d37
ms.date: 12/05/2018
ms.keywords: WsGetNamespaceFromPrefix, WsGetNamespaceFromPrefix function [Web Services for Windows], webservices/WsGetNamespaceFromPrefix, wsw.wsgetnamespacefromprefix
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
 - WsGetNamespaceFromPrefix
 - webservices/WsGetNamespaceFromPrefix
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
 - WsGetNamespaceFromPrefix
---

# WsGetNamespaceFromPrefix function


## -description

This function returns a namespace from the prefix to which it is bound.
      

If the value of the <i>required</i> parameter is set to <b>TRUE</b> and the Prefix is not bound to any namespace a <b>WS_E_INVALID_FORMAT</b> exception will be returned.
        (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.) If the <i>required</i> parameter is  <b>FALSE</b>, and the Prefix is not bound to any namespace the <i>ns</i> parameter will be <b>NULL</b> and the function will return S_FALSE.

## -parameters

### -param reader [in]

A pointer to the reader for which the prefix should be searched.

### -param prefix [in]

A pointer to the Prefix to search for.

### -param required [in]

The value of this Boolean parameter determines
          whether or not an error should be returned if a matching namespace is not found.

### -param ns

A reference to a namespace to which the prefix is bound if successful.  The value returned is valid only until the writer advances.

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

For the prefix "xml" it will return the namespace "http://www.w3.org/XML/1998/namespace".
      

For the prefix "xmlns" it will return the namespace "http://www.w3.org/2000/xmlns/".