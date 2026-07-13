---
UID: NF:xpsobjectmodel.IXpsOMCanvas.GetDictionary
title: IXpsOMCanvas::GetDictionary (xpsobjectmodel.h)
description: Gets a pointer to the resolved IXpsOMDictionary interface of the dictionary associated with the canvas.
helpviewer_keywords: ["GetDictionary","GetDictionary method [XPS Documents and Packaging]","GetDictionary method [XPS Documents and Packaging]","IXpsOMCanvas interface","IXpsOMCanvas interface [XPS Documents and Packaging]","GetDictionary method","IXpsOMCanvas.GetDictionary","IXpsOMCanvas::GetDictionary","xps.ixpsomcanvas_getdictionary","xpsobjectmodel/IXpsOMCanvas::GetDictionary"]
old-location: xps\ixpsomcanvas_getdictionary.htm
tech.root: xps
ms.assetid: f32b534e-92bf-4e80-9ac1-b2577e076bed
ms.date: 12/05/2018
ms.keywords: GetDictionary, GetDictionary method [XPS Documents and Packaging], GetDictionary method [XPS Documents and Packaging],IXpsOMCanvas interface, IXpsOMCanvas interface [XPS Documents and Packaging],GetDictionary method, IXpsOMCanvas.GetDictionary, IXpsOMCanvas::GetDictionary, xps.ixpsomcanvas_getdictionary, xpsobjectmodel/IXpsOMCanvas::GetDictionary
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
 - IXpsOMCanvas::GetDictionary
 - xpsobjectmodel/IXpsOMCanvas::GetDictionary
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
 - IXpsOMCanvas.GetDictionary
---

# IXpsOMCanvas::GetDictionary


## -description

Gets a pointer to the resolved <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface of the dictionary associated with the canvas.

## -parameters

### -param resourceDictionary [out, retval]

A pointer to the resolved <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface of the dictionary.

The value that is returned in this parameter depends on which method has been most recently called to set the dictionary.

<table>
<tr>
<th>Most recent method called</th>
<th>Object returned in <i>resourceDictionary</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionarylocal">SetDictionaryLocal</a>


</td>
<td>
The local dictionary  that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionarylocal">SetDictionaryLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionaryresource">SetDictionaryResource</a>


</td>
<td>
The shared dictionary in the dictionary resource that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionaryresource">SetDictionaryResource</a>.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionarylocal">SetDictionaryLocal</a> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionaryresource">SetDictionaryResource</a> has been called yet.

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
</table>

## -remarks

<b>GetDictionary</b> can return the interface pointer of a local or remote dictionary.  <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdictionary-getowner">GetOwner</a> can be called to determine whether the dictionary is local or remote.

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>