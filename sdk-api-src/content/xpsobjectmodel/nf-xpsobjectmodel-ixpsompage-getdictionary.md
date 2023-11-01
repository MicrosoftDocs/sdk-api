---
UID: NF:xpsobjectmodel.IXpsOMPage.GetDictionary
title: IXpsOMPage::GetDictionary (xpsobjectmodel.h)
description: Gets a pointer to the resolved IXpsOMDictionary interface that is associated with this page.
helpviewer_keywords: ["GetDictionary","GetDictionary method [XPS Documents and Packaging]","GetDictionary method [XPS Documents and Packaging]","IXpsOMPage interface","IXpsOMPage interface [XPS Documents and Packaging]","GetDictionary method","IXpsOMPage.GetDictionary","IXpsOMPage::GetDictionary","xps.ixpsompage_getdictionary","xpsobjectmodel/IXpsOMPage::GetDictionary"]
old-location: xps\ixpsompage_getdictionary.htm
tech.root: xps
ms.assetid: e842c828-6e8c-4190-b845-8c8a26af1579
ms.date: 12/05/2018
ms.keywords: GetDictionary, GetDictionary method [XPS Documents and Packaging], GetDictionary method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetDictionary method, IXpsOMPage.GetDictionary, IXpsOMPage::GetDictionary, xps.ixpsompage_getdictionary, xpsobjectmodel/IXpsOMPage::GetDictionary
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMPage::GetDictionary
 - xpsobjectmodel/IXpsOMPage::GetDictionary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPage.GetDictionary
---

# IXpsOMPage::GetDictionary


## -description

Gets a pointer to the resolved <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface that is associated with this page.

## -parameters

### -param resourceDictionary [out, retval]

A pointer to the resolved <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface that is associated with this page.

The value that is returned in this parameter depends on which method has most recently been called to set the dictionary.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>resourceDictionary</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionarylocal">SetDictionaryLocal</a>


</td>
<td>
The local dictionary resource that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionarylocal">SetDictionaryLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionaryresource">SetDictionaryResource</a>


</td>
<td>
The shared dictionary in the dictionary resource that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionaryresource">SetDictionaryResource</a>.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionarylocal">SetDictionaryLocal</a> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionaryresource">SetDictionaryResource</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>resourceDictionary</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_INVALID_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The lookup key name set by  <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a> references an object that is not a brush.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matched the lookup value.

No object could be found with a key name that matched the value passed in <i>lookup</i>.

</td>
</tr>
</table>

## -remarks

Whether the dictionary is local or is contained within a remote dictionary resource, this method returns an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface pointer. <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdictionary-getowner">GetOwner</a> determines whether the dictionary  is remote.

If a page contains a remote dictionary, <b>GetDictionary</b> will deserialize the dictionary. If the page contains a remote dictionary that is not valid, <b>GetDictionary</b> might return a deserialization error code.

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>