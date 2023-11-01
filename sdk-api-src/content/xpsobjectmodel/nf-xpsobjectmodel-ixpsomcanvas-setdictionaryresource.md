---
UID: NF:xpsobjectmodel.IXpsOMCanvas.SetDictionaryResource
title: IXpsOMCanvas::SetDictionaryResource (xpsobjectmodel.h)
description: Sets the IXpsOMRemoteDictionaryResource interface pointer of the remote dictionary resource.
helpviewer_keywords: ["IXpsOMCanvas interface [XPS Documents and Packaging]","SetDictionaryResource method","IXpsOMCanvas.SetDictionaryResource","IXpsOMCanvas::SetDictionaryResource","SetDictionaryResource","SetDictionaryResource method [XPS Documents and Packaging]","SetDictionaryResource method [XPS Documents and Packaging]","IXpsOMCanvas interface","xps.ixpsomcanvas_setdictionaryresource","xpsobjectmodel/IXpsOMCanvas::SetDictionaryResource"]
old-location: xps\ixpsomcanvas_setdictionaryresource.htm
tech.root: xps
ms.assetid: 8f6a80e9-fa66-45fa-bee9-c80a64a4593f
ms.date: 12/05/2018
ms.keywords: IXpsOMCanvas interface [XPS Documents and Packaging],SetDictionaryResource method, IXpsOMCanvas.SetDictionaryResource, IXpsOMCanvas::SetDictionaryResource, SetDictionaryResource, SetDictionaryResource method [XPS Documents and Packaging], SetDictionaryResource method [XPS Documents and Packaging],IXpsOMCanvas interface, xps.ixpsomcanvas_setdictionaryresource, xpsobjectmodel/IXpsOMCanvas::SetDictionaryResource
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
 - IXpsOMCanvas::SetDictionaryResource
 - xpsobjectmodel/IXpsOMCanvas::SetDictionaryResource
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
 - IXpsOMCanvas.SetDictionaryResource
---

# IXpsOMCanvas::SetDictionaryResource


## -description

Sets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer of the remote dictionary resource.

## -parameters

### -param remoteDictionaryResource [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface of the remote dictionary resource. A <b>NULL</b> pointer releases any previously assigned dictionary resource.

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

After calling this method,  <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getdictionarylocal">GetDictionaryLocal</a>  returns a <b>NULL</b> pointer in the <i>resourceDictionary</i> parameter.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>resourceDictionary</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getdictionary">GetDictionary</a>
</th>
<th>Object that is returned in <i>resourceDictionary</i>     by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getdictionarylocal">GetDictionaryLocal</a>
</th>
<th>Object that is returned in  <i>remoteDictionaryResource</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getdictionaryresource">GetDictionaryResource</a>
</th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionarylocal">SetDictionaryLocal</a>


</td>
<td>
The local dictionary that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionarylocal">SetDictionaryLocal</a>.

</td>
<td>
The local dictionary that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionarylocal">SetDictionaryLocal</a>.

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
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionarylocal">SetDictionaryLocal</a> nor <b>SetDictionaryResource</b> has been called yet.

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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>