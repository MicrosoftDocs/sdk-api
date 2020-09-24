---
UID: NF:wsdutil.WSDXMLAddSibling
title: WSDXMLAddSibling function (wsdutil.h)
description: Adds a sibling element.
helpviewer_keywords: ["WSDXMLAddSibling","WSDXMLAddSibling function","ncd.wsdxmladdsibling","wsdutil/WSDXMLAddSibling"]
old-location: ncd\wsdxmladdsibling.htm
tech.root: ncd
ms.assetid: dbe5de39-eb8e-4352-b0c4-32d10e324185
ms.date: 12/05/2018
ms.keywords: WSDXMLAddSibling, WSDXMLAddSibling function, ncd.wsdxmladdsibling, wsdutil/WSDXMLAddSibling
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
 - WSDXMLAddSibling
 - wsdutil/WSDXMLAddSibling
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
 - WSDXMLAddSibling
---

# WSDXMLAddSibling function


## -description

Adds a sibling element.

## -parameters

### -param pFirst [in]

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that contains the first sibling.

### -param pSecond [in]

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that contains the second sibling.

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
<i>pFirst</i> or <i>pSecond</i> is <b>NULL</b>.

</td>
</tr>
</table>