---
UID: NF:xpsobjectmodel.IXpsOMPage.GetDictionaryResource
title: IXpsOMPage::GetDictionaryResource (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMRemoteDictionaryResource interface of the shared dictionary resource that is used by this page.
helpviewer_keywords: ["GetDictionaryResource","GetDictionaryResource method [XPS Documents and Packaging]","GetDictionaryResource method [XPS Documents and Packaging]","IXpsOMPage interface","IXpsOMPage interface [XPS Documents and Packaging]","GetDictionaryResource method","IXpsOMPage.GetDictionaryResource","IXpsOMPage::GetDictionaryResource","xps.ixpsompage_getdictionaryresource","xpsobjectmodel/IXpsOMPage::GetDictionaryResource"]
old-location: xps\ixpsompage_getdictionaryresource.htm
tech.root: xps
ms.assetid: 12313d19-e6f1-4ec3-9702-2a403087763a
ms.date: 12/05/2018
ms.keywords: GetDictionaryResource, GetDictionaryResource method [XPS Documents and Packaging], GetDictionaryResource method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetDictionaryResource method, IXpsOMPage.GetDictionaryResource, IXpsOMPage::GetDictionaryResource, xps.ixpsompage_getdictionaryresource, xpsobjectmodel/IXpsOMPage::GetDictionaryResource
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
 - IXpsOMPage::GetDictionaryResource
 - xpsobjectmodel/IXpsOMPage::GetDictionaryResource
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
 - IXpsOMPage.GetDictionaryResource
---

# IXpsOMPage::GetDictionaryResource


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface of the shared dictionary resource that is used by this page.

## -parameters

### -param remoteDictionaryResource [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface of the shared dictionary resource that is used by this page. If no <b>IXpsOMRemoteDictionaryResource</b> interface has been set or if a local dictionary has been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>remoteDictionaryResource</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionarylocal">SetDictionaryLocal</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionaryresource">SetDictionaryResource</a>


</td>
<td>
The remote dictionary resource that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionaryresource">SetDictionaryResource</a>.

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
<i>remoteDictionaryResource</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>