---
UID: NF:webservices.WsReadQualifiedName
title: WsReadQualifiedName function (webservices.h)
description: Reads a qualified name and separates it into its prefix, localName and namespace based on the current namespace scope of the XML_READER.
helpviewer_keywords: ["WsReadQualifiedName","WsReadQualifiedName function [Web Services for Windows]","webservices/WsReadQualifiedName","wsw.wsreadqualifiedname"]
old-location: wsw\wsreadqualifiedname.htm
tech.root: wsw
ms.assetid: bc49fb89-72ba-435a-ac50-303f16d36da2
ms.date: 12/05/2018
ms.keywords: WsReadQualifiedName, WsReadQualifiedName function [Web Services for Windows], webservices/WsReadQualifiedName, wsw.wsreadqualifiedname
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
 - WsReadQualifiedName
 - webservices/WsReadQualifiedName
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
 - WsReadQualifiedName
---

# WsReadQualifiedName function


## -description

Reads a qualified name and separates it into its prefix, localName 
        and namespace based on the current namespace scope of the XML_READER. 
        If the ns parameter is specified, then the namespace that the prefix 
        is bound to will be returned, or <b>WS_E_INVALID_FORMAT</b> will be returned. (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.) The strings are placed in the specified heap.

## -parameters

### -param reader [in]

The reader which should read the qualified name.

### -param heap [in]

The heap on which the resulting strings should be allocated.

### -param prefix

The prefix of the qualified name is returned here.

### -param localName [out]

The localName of the qualified name is returned here.

### -param ns

The namespace to which the qualified name is bound is returned here.

### -param error [in, optional]

If the localName is missing the function will return <b>WS_E_INVALID_FORMAT</b>.  
          If the ns parameter is specified, but the prefix is not bound to a namespace, 
           <b>WS_E_INVALID_FORMAT</b> will be returned.

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