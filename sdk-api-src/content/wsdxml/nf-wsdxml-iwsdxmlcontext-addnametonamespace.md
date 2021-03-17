---
UID: NF:wsdxml.IWSDXMLContext.AddNameToNamespace
title: IWSDXMLContext::AddNameToNamespace (wsdxml.h)
description: Creates an object that represents a name in a namespace in an XML context.
helpviewer_keywords: ["AddNameToNamespace","AddNameToNamespace method","AddNameToNamespace method","IWSDXMLContext interface","IWSDXMLContext interface","AddNameToNamespace method","IWSDXMLContext.AddNameToNamespace","IWSDXMLContext::AddNameToNamespace","ncd.iwsdxmlcontext_addnametonamespace_method","wsdxml/IWSDXMLContext::AddNameToNamespace"]
old-location: ncd\iwsdxmlcontext_addnametonamespace_method.htm
tech.root: ncd
ms.assetid: d480f868-46ab-4d9c-ae52-4e5ca5cb9fd9
ms.date: 12/05/2018
ms.keywords: AddNameToNamespace, AddNameToNamespace method, AddNameToNamespace method,IWSDXMLContext interface, IWSDXMLContext interface,AddNameToNamespace method, IWSDXMLContext.AddNameToNamespace, IWSDXMLContext::AddNameToNamespace, ncd.iwsdxmlcontext_addnametonamespace_method, wsdxml/IWSDXMLContext::AddNameToNamespace
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
 - IWSDXMLContext::AddNameToNamespace
 - wsdxml/IWSDXMLContext::AddNameToNamespace
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
 - IWSDXMLContext.AddNameToNamespace
---

# IWSDXMLContext::AddNameToNamespace


## -description

Creates an object that represents a name in a namespace in an XML context. If the name already exists in the namespace, no new name will be added, and the name object for the existing name will be returned.

## -parameters

### -param pszUri [in]

The URI of the XML namespace in which this name will be created. If this namespace does not already exist in the XML context, a new namespace structure will be generated automatically.

### -param pszName [in]

The name to add to the namespace specified by <i>pszUri</i>.

### -param ppName [out]

A <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_name">WSDXML_NAME</a> structure for the newly created name. You must deallocate <i>ppName</i> by calling <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a>. This parameter is optional.

## -returns

Possible return values include, but are not limited to, the following.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszUri</i> is <b>NULL</b> or the length in characters of the URI string exceeds WSD_MAX_TEXT_LENGTH (8192). <i>pszName</i> is <b>NULL</b> or the length in characters of the name string exceeds WSD_MAX_TEXT_LENGTH (8192).

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

## -remarks

<b>AddNameToNamespace</b> can be used when creating XML elements for extensible sections. Extensible sections are represented by the <b>any</b> element in a schema. The returned <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_name">WSDXML_NAME</a> structure pointed to by <i>ppName</i> can be used to specify the name associated with the extension content. When building a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that represents extension content, use the returned <b>WSDXML_NAME</b> structure for the element's  <b>Name</b> member.

## -see-also

<a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a>