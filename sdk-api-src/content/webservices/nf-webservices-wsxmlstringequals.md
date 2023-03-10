---
UID: NF:webservices.WsXmlStringEquals
title: WsXmlStringEquals function (webservices.h)
description: Compares two WS_XML_STRING objects for equality. The operation performs an ordinal comparison of the character values contained by the String objects.
helpviewer_keywords: ["WsXmlStringEquals","WsXmlStringEquals function [Web Services for Windows]","webservices/WsXmlStringEquals","wsw.wsxmlstringequals"]
old-location: wsw\wsxmlstringequals.htm
tech.root: wsw
ms.assetid: 4fcff6d7-b17c-4cd6-9671-1aff7b84fa98
ms.date: 12/05/2018
ms.keywords: WsXmlStringEquals, WsXmlStringEquals function [Web Services for Windows], webservices/WsXmlStringEquals, wsw.wsxmlstringequals
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
 - WsXmlStringEquals
 - webservices/WsXmlStringEquals
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
 - WsXmlStringEquals
---

# WsXmlStringEquals function


## -description

Compares two <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a> objects for equality.  The operation performs an ordinal comparison
        of the character values contained by the String objects.

## -parameters

### -param string1 [in]

A pointer to the first string to compare.

### -param string2 [in]

A pointer to the second string to compare.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The strings are equal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The strings are not equal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not correct.

</td>
</tr>
</table>

## -remarks

This function is typically used to compare localNames and namespaces in XML.