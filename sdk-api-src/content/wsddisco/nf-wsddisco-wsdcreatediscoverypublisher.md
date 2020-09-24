---
UID: NF:wsddisco.WSDCreateDiscoveryPublisher
title: WSDCreateDiscoveryPublisher function (wsddisco.h)
description: Creates an IWSDiscoveryPublisher object.
helpviewer_keywords: ["WSDCreateDiscoveryPublisher","WSDCreateDiscoveryPublisher function","ncd.wsdcreatediscoverypublisher_func","wsddisco/WSDCreateDiscoveryPublisher"]
old-location: ncd\wsdcreatediscoverypublisher_func.htm
tech.root: ncd
ms.assetid: 18abde49-2ea7-4c49-9afe-1b7c7182aeeb
ms.date: 12/05/2018
ms.keywords: WSDCreateDiscoveryPublisher, WSDCreateDiscoveryPublisher function, ncd.wsdcreatediscoverypublisher_func, wsddisco/WSDCreateDiscoveryPublisher
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSDCreateDiscoveryPublisher
 - wsddisco/WSDCreateDiscoveryPublisher
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDCreateDiscoveryPublisher
---

# WSDCreateDiscoveryPublisher function


## -description

Creates an <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a> object.

## -parameters

### -param pContext [in]

An <a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a> interface that defines custom message types or namespaces. 

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.

### -param ppPublisher [out]

Returns a reference to the initialized <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a> object. Cannot be <b>NULL</b>.

## -returns

Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppPublisher</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>