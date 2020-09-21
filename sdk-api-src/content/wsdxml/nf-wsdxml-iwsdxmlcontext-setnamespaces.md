---
UID: NF:wsdxml.IWSDXMLContext.SetNamespaces
title: IWSDXMLContext::SetNamespaces (wsdxml.h)
description: Associates custom namespaces with the XML context object.
helpviewer_keywords: ["IWSDXMLContext interface","SetNamespaces method","IWSDXMLContext.SetNamespaces","IWSDXMLContext::SetNamespaces","SetNamespaces","SetNamespaces method","SetNamespaces method","IWSDXMLContext interface","ncd.iwsdxmlcontext_setnamespaces_method","wsdxml/IWSDXMLContext::SetNamespaces"]
old-location: ncd\iwsdxmlcontext_setnamespaces_method.htm
tech.root: ncd
ms.assetid: 94ec94d1-e0d8-42cb-993f-6da9c8df1a47
ms.date: 12/05/2018
ms.keywords: IWSDXMLContext interface,SetNamespaces method, IWSDXMLContext.SetNamespaces, IWSDXMLContext::SetNamespaces, SetNamespaces, SetNamespaces method, SetNamespaces method,IWSDXMLContext interface, ncd.iwsdxmlcontext_setnamespaces_method, wsdxml/IWSDXMLContext::SetNamespaces
req.header: wsdxml.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdXml.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDXMLContext::SetNamespaces
 - wsdxml/IWSDXMLContext::SetNamespaces
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDXMLContext.SetNamespaces
---

# IWSDXMLContext::SetNamespaces


## -description

Associates custom namespaces with the XML context object. 

This method should only be called by <a href="/windows/desktop/WsdApi/web-services-for-devices-code-generator">generated code</a>, and should not be called directly by a WSDAPI client. Instead, the code generator will provide wrappers that access this method properly.

## -parameters

### -param pNamespaces [in]

An array of <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_namespace">WSDXML_NAMESPACE</a> structures.

### -param wNamespacesCount [in]

The number of namespaces in the <i>pNamespaces</i> array.

### -param bLayerNumber [in]

The layer number associated with the <a href="/windows/desktop/WsdApi/web-services-for-devices-code-generator">generated service code</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pNamespaces</i> is <b>NULL</b> or  <i>bLayerNumber</i> is greater than or equal to WSD_XMLCONTEXT_NUM_LAYERS (16).

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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a>