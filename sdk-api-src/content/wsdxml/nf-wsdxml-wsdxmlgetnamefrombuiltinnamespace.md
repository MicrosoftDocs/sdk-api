---
UID: NF:wsdxml.WSDXMLGetNameFromBuiltinNamespace
title: WSDXMLGetNameFromBuiltinNamespace function (wsdxml.h)
description: Gets a specified name from the built-in namespace.
helpviewer_keywords: ["WSDXMLGetNameFromBuiltinNamespace","WSDXMLGetNameFromBuiltinNamespace function","ncd.wsdxmlgetnamefrombuiltinnamespace","wsdxml/WSDXMLGetNameFromBuiltinNamespace"]
old-location: ncd\wsdxmlgetnamefrombuiltinnamespace.htm
tech.root: ncd
ms.assetid: b7a5ac45-ee87-4290-9cbb-de523c0f2775
ms.date: 12/05/2018
ms.keywords: WSDXMLGetNameFromBuiltinNamespace, WSDXMLGetNameFromBuiltinNamespace function, ncd.wsdxmlgetnamefrombuiltinnamespace, wsdxml/WSDXMLGetNameFromBuiltinNamespace
req.header: wsdxml.h
req.include-header: 
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
 - WSDXMLGetNameFromBuiltinNamespace
 - wsdxml/WSDXMLGetNameFromBuiltinNamespace
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
 - WSDXMLGetNameFromBuiltinNamespace
---

# WSDXMLGetNameFromBuiltinNamespace function


## -description

Gets a specified name from the built-in namespace.

## -parameters

### -param pszNamespace

The namespace to match with a built-in namespace.

### -param pszName

The name to match with a built-in name.

### -param ppName

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_name">WSDXML_NAME</a> structure that contains the returned built-in name.  The memory usage of <i>ppName</i> is managed elsewhere.  Consequently, the calling application should not attempt to deallocate <i>ppName</i>.

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszNamespace</i> is <b>NULL</b>, <i>pszName</i> is <b>NULL</b>, the length in characters of <i>pszNamespace</i> exceeds WSD_MAX_TEXT_LENGTH (8192), the length in characters of <i>pszName</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or there was no matching name in the built-in namespace.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppName</i> is <b>NULL</b>.

</td>
</tr>
</table>