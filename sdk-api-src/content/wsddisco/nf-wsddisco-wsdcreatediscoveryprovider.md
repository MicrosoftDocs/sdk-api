---
UID: NF:wsddisco.WSDCreateDiscoveryProvider
title: WSDCreateDiscoveryProvider function (wsddisco.h)
description: Creates an IWSDiscoveryProvider object.
helpviewer_keywords: ["WSDCreateDiscoveryProvider","WSDCreateDiscoveryProvider function","ncd.wsdcreatediscoveryprovider_func","wsddisco/WSDCreateDiscoveryProvider"]
old-location: ncd\wsdcreatediscoveryprovider_func.htm
tech.root: ncd
ms.assetid: 44275cbe-ea02-41fd-b88d-81d4df966067
ms.date: 12/05/2018
ms.keywords: WSDCreateDiscoveryProvider, WSDCreateDiscoveryProvider function, ncd.wsdcreatediscoveryprovider_func, wsddisco/WSDCreateDiscoveryProvider
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
 - WSDCreateDiscoveryProvider
 - wsddisco/WSDCreateDiscoveryProvider
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
 - WSDCreateDiscoveryProvider
---

# WSDCreateDiscoveryProvider function


## -description

Creates an <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a> object.

## -parameters

### -param pContext [in]

An <a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a> interface that defines custom message types or namespaces. 

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.

### -param ppProvider [out]

Returns a reference to the initialized <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a> object. Cannot be <b>NULL</b>.

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
</table>