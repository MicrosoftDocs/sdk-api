---
UID: NF:xpsobjectmodel.IXpsOMPage.SetDictionaryResource
title: IXpsOMPage::SetDictionaryResource (xpsobjectmodel.h)
description: Sets the IXpsOMRemoteDictionaryResource interface pointer of the page's remote dictionary resource.
helpviewer_keywords: ["IXpsOMPage interface [XPS Documents and Packaging]","SetDictionaryResource method","IXpsOMPage.SetDictionaryResource","IXpsOMPage::SetDictionaryResource","SetDictionaryResource","SetDictionaryResource method [XPS Documents and Packaging]","SetDictionaryResource method [XPS Documents and Packaging]","IXpsOMPage interface","xps.ixpsompage_setdictionaryresource","xpsobjectmodel/IXpsOMPage::SetDictionaryResource"]
old-location: xps\ixpsompage_setdictionaryresource.htm
tech.root: xps
ms.assetid: e424c70e-289c-4519-8b20-5fb98d46bf34
ms.date: 12/05/2018
ms.keywords: IXpsOMPage interface [XPS Documents and Packaging],SetDictionaryResource method, IXpsOMPage.SetDictionaryResource, IXpsOMPage::SetDictionaryResource, SetDictionaryResource, SetDictionaryResource method [XPS Documents and Packaging], SetDictionaryResource method [XPS Documents and Packaging],IXpsOMPage interface, xps.ixpsompage_setdictionaryresource, xpsobjectmodel/IXpsOMPage::SetDictionaryResource
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
 - IXpsOMPage::SetDictionaryResource
 - xpsobjectmodel/IXpsOMPage::SetDictionaryResource
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
 - IXpsOMPage.SetDictionaryResource
---

# IXpsOMPage::SetDictionaryResource


## -description

Sets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer of the page's remote dictionary resource.

## -parameters

### -param remoteDictionaryResource [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer to be set for the page. A <b>NULL</b> value releases the previously assigned dictionary resource.

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
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>remoteDictionaryResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

Setting this value will cause <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getdictionarylocal">GetDictionaryLocal</a> to return <b>NULL</b>.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>resourceDictionary</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getdictionary">GetDictionary</a>
</th>
<th>Object that is returned in <i>resourceDictionary</i>  by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getdictionarylocal">GetDictionaryLocal</a>
</th>
<th>Object that is returned in <i>remoteDictionaryResource</i>   by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getdictionaryresource">GetDictionaryResource</a>
</th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionarylocal">SetDictionaryLocal</a>


</td>
<td>
The local dictionary resource that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionarylocal">SetDictionaryLocal</a>.

</td>
<td>
The local dictionary resource that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionarylocal">SetDictionaryLocal</a>.

</td>
<td>
<b>NULL</b> pointer. 

</td>
</tr>
<tr>
<td>
<b>SetDictionaryResource</b> (this method)

</td>
<td>
The shared dictionary in the dictionary resource that is set by <b>SetDictionaryResource</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The remote dictionary resource that is set by <b>SetDictionaryResource</b>.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionarylocal">SetDictionaryLocal</a> nor <b>SetDictionaryResource</b> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>