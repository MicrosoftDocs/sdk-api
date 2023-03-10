---
UID: NF:wsdutil.WSDXMLAddChild
title: WSDXMLAddChild function (wsdutil.h)
description: Adds a child element.
helpviewer_keywords: ["WSDXMLAddChild","WSDXMLAddChild function","ncd.wsdxmladdchild","wsdutil/WSDXMLAddChild"]
old-location: ncd\wsdxmladdchild.htm
tech.root: ncd
ms.assetid: a0688b03-6f91-4b8e-88d1-b40af69fe8bb
ms.date: 12/05/2018
ms.keywords: WSDXMLAddChild, WSDXMLAddChild function, ncd.wsdxmladdchild, wsdutil/WSDXMLAddChild
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
 - WSDXMLAddChild
 - wsdutil/WSDXMLAddChild
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
 - WSDXMLAddChild
---

# WSDXMLAddChild function


## -description

Adds a child element.

## -parameters

### -param pParent

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that contains the parent element.

### -param pChild

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that contains the child element.

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
<i>pParent</i> is <b>NULL</b>, <i>pChild</i> is <b>NULL</b>, <i>pChild</i> already has a parent, or a sibling could not be added to an existing child of <i>pParent</i>.

</td>
</tr>
</table>