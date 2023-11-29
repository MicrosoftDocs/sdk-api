---
UID: NF:xpsobjectmodel.IXpsOMPage.SetDictionaryLocal
title: IXpsOMPage::SetDictionaryLocal (xpsobjectmodel.h)
description: Sets the IXpsOMDictionary interface pointer of the page's local dictionary resource.
helpviewer_keywords: ["IXpsOMPage interface [XPS Documents and Packaging]","SetDictionaryLocal method","IXpsOMPage.SetDictionaryLocal","IXpsOMPage::SetDictionaryLocal","SetDictionaryLocal","SetDictionaryLocal method [XPS Documents and Packaging]","SetDictionaryLocal method [XPS Documents and Packaging]","IXpsOMPage interface","xps.ixpsompage_setdictionarylocal","xpsobjectmodel/IXpsOMPage::SetDictionaryLocal"]
old-location: xps\ixpsompage_setdictionarylocal.htm
tech.root: xps
ms.assetid: d950a21a-0afe-410a-9f2c-32847c35471e
ms.date: 12/05/2018
ms.keywords: IXpsOMPage interface [XPS Documents and Packaging],SetDictionaryLocal method, IXpsOMPage.SetDictionaryLocal, IXpsOMPage::SetDictionaryLocal, SetDictionaryLocal, SetDictionaryLocal method [XPS Documents and Packaging], SetDictionaryLocal method [XPS Documents and Packaging],IXpsOMPage interface, xps.ixpsompage_setdictionarylocal, xpsobjectmodel/IXpsOMPage::SetDictionaryLocal
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
 - IXpsOMPage::SetDictionaryLocal
 - xpsobjectmodel/IXpsOMPage::SetDictionaryLocal
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
 - IXpsOMPage.SetDictionaryLocal
---

# IXpsOMPage::SetDictionaryLocal


## -description

Sets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface pointer of the page's local dictionary resource.

## -parameters

### -param resourceDictionary [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface pointer to be set for the page. A <b>NULL</b> pointer releases any previously assigned local dictionary.

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
<i>resourceDictionary</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

After you call <b>SetDictionaryLocal</b>, the remote dictionary resource is released and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getdictionaryresource">GetDictionaryResource</a> returns a <b>NULL</b> pointer in the <i>remoteDictionaryResource</i> parameter. The table that follows explains the relationship between the local and remote values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in <i>resourceDictionary</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getdictionary">GetDictionary</a>
</th>
<th>Object that is returned  in <i>resourceDictionary</i>      by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getdictionarylocal">GetDictionaryLocal</a>
</th>
<th>Object that is returned  in <i>remoteDictionaryResource</i>  by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getdictionaryresource">GetDictionaryResource</a>
</th>
</tr>
<tr>
<td>
<b>SetDictionaryLocal</b> (this method)

</td>
<td>
The local dictionary resource that is set by <b>SetDictionaryLocal</b>.

</td>
<td>
The local dictionary resource that is set by <b>SetDictionaryLocal</b>.

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
The shared dictionary in the dictionary resource that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionaryresource">SetDictionaryResource</a>.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The remote dictionary resource that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionaryresource">SetDictionaryResource</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetDictionaryLocal</b> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-setdictionaryresource">SetDictionaryResource</a> has been called yet.

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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>