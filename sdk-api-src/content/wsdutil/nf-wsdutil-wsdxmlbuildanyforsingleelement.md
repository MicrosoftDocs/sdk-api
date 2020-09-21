---
UID: NF:wsdutil.WSDXMLBuildAnyForSingleElement
title: WSDXMLBuildAnyForSingleElement function (wsdutil.h)
description: Creates an XML element with a specified name and value.
helpviewer_keywords: ["WSDXMLBuildAnyForSingleElement","WSDXMLBuildAnyForSingleElement function","ncd.wsdxmlbuildanyforsingleelement","wsdutil/WSDXMLBuildAnyForSingleElement"]
old-location: ncd\wsdxmlbuildanyforsingleelement.htm
tech.root: ncd
ms.assetid: 2a8b9b4a-0a08-442a-896f-f980bff28f03
ms.date: 12/05/2018
ms.keywords: WSDXMLBuildAnyForSingleElement, WSDXMLBuildAnyForSingleElement function, ncd.wsdxmlbuildanyforsingleelement, wsdutil/WSDXMLBuildAnyForSingleElement
req.header: wsdutil.h
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
 - WSDXMLBuildAnyForSingleElement
 - wsdutil/WSDXMLBuildAnyForSingleElement
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
 - WSDXMLBuildAnyForSingleElement
---

# WSDXMLBuildAnyForSingleElement function


## -description

Creates an XML element with a specified name and value.  The created element can be used as the child of an XML <b>any</b>  element.

## -parameters

### -param pElementName [in]

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_name">WSDXML_NAME</a> structure that contains the name of the  created element.

### -param pszText [in]

The text value of the created element.

### -param ppAny [out]

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> that contains the created element.  <i>ppAny</i> must be freed with a call to <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a>.

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
<i>pElementName</i> is <b>NULL</b> or the length in characters of <i>pszText</i> exceeds WSD_MAX_TEXT_LENGTH (8192).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAny</i> is <b>NULL</b>.

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