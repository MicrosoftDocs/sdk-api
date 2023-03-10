---
UID: NF:wsddisco.WSDCreateDiscoveryProvider2
title: WSDCreateDiscoveryProvider2 function (wsddisco.h)
description: Creates an IWSDiscoveryProvider object that supports signed messages.
helpviewer_keywords: ["WSDCreateDiscoveryProvider2","WSDCreateDiscoveryProvider2 function","ncd.wsdcreatediscoveryprovider2","wsddisco/WSDCreateDiscoveryProvider2"]
old-location: ncd\wsdcreatediscoveryprovider2.htm
tech.root: ncd
ms.assetid: dc757897-032c-4ea3-8f4e-cf00d4ec385b
ms.date: 12/05/2018
ms.keywords: WSDCreateDiscoveryProvider2, WSDCreateDiscoveryProvider2 function, ncd.wsdcreatediscoveryprovider2, wsddisco/WSDCreateDiscoveryProvider2
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
 - WSDCreateDiscoveryProvider2
 - wsddisco/WSDCreateDiscoveryProvider2
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
 - WSDCreateDiscoveryProvider2
---

# WSDCreateDiscoveryProvider2 function


## -description

Creates an <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a> object that supports signed messages.

## -parameters

### -param pContext [in]

An <a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a> interface that defines custom message types or namespaces.

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.

### -param pConfigParams [in]

An array of <a href="/windows/desktop/api/wsdbase/ns-wsdbase-wsd_config_param">WSD_CONFIG_PARAM</a> structures that contain the parameters for creating the object.

### -param dwConfigParamCount [in]

The total number of structures passed in <i>pConfigParams</i>.

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
Function completed successfully.

</td>
</tr>
</table>