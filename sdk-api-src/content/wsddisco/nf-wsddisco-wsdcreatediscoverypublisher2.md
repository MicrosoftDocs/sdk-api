---
UID: NF:wsddisco.WSDCreateDiscoveryPublisher2
title: WSDCreateDiscoveryPublisher2 function (wsddisco.h)
description: Creates an IWSDiscoveryPublisher object that supports signed messages.
helpviewer_keywords: ["WSDCreateDiscoveryPublisher2","WSDCreateDiscoveryPublisher2 function","ncd.wsdcreatediscoverypublisher2","wsddisco/WSDCreateDiscoveryPublisher2"]
old-location: ncd\wsdcreatediscoverypublisher2.htm
tech.root: ncd
ms.assetid: 43c17910-a4b6-4889-ba98-4e125b4a3ac0
ms.date: 12/05/2018
ms.keywords: WSDCreateDiscoveryPublisher2, WSDCreateDiscoveryPublisher2 function, ncd.wsdcreatediscoverypublisher2, wsddisco/WSDCreateDiscoveryPublisher2
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WSDCreateDiscoveryPublisher2
 - wsddisco/WSDCreateDiscoveryPublisher2
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
 - WSDCreateDiscoveryPublisher2
---

# WSDCreateDiscoveryPublisher2 function


## -description

Creates an <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a> object that supports signed messages.

## -parameters

### -param pContext [in]

An <a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a> interface that defines custom message types or namespaces.

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.

### -param pConfigParams [in]

An array of <a href="/windows/desktop/api/wsdbase/ns-wsdbase-wsd_config_param">WSD_CONFIG_PARAM</a> structures that contain the parameters for creating the object.

### -param dwConfigParamCount [in]

The total number of structures passed in <i>pConfigParams</i>.

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
Function completed successfully.

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