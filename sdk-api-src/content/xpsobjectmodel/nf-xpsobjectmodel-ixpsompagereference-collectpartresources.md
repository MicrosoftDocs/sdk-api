---
UID: NF:xpsobjectmodel.IXpsOMPageReference.CollectPartResources
title: IXpsOMPageReference::CollectPartResources (xpsobjectmodel.h)
description: Creates a list of all part-based resources that are associated with the page.
helpviewer_keywords: ["CollectPartResources","CollectPartResources method [XPS Documents and Packaging]","CollectPartResources method [XPS Documents and Packaging]","IXpsOMPageReference interface","IXpsOMPageReference interface [XPS Documents and Packaging]","CollectPartResources method","IXpsOMPageReference.CollectPartResources","IXpsOMPageReference::CollectPartResources","xps.ixpsompagereference_collectpartresources","xpsobjectmodel/IXpsOMPageReference::CollectPartResources"]
old-location: xps\ixpsompagereference_collectpartresources.htm
tech.root: xps
ms.assetid: 52a45351-669c-42f3-b02b-afbf42727313
ms.date: 12/05/2018
ms.keywords: CollectPartResources, CollectPartResources method [XPS Documents and Packaging], CollectPartResources method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],CollectPartResources method, IXpsOMPageReference.CollectPartResources, IXpsOMPageReference::CollectPartResources, xps.ixpsompagereference_collectpartresources, xpsobjectmodel/IXpsOMPageReference::CollectPartResources
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
 - IXpsOMPageReference::CollectPartResources
 - xpsobjectmodel/IXpsOMPageReference::CollectPartResources
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
 - IXpsOMPageReference.CollectPartResources
---

# IXpsOMPageReference::CollectPartResources


## -description

Creates a list of all part-based resources that are associated with the page.

## -parameters

### -param partResources [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a> interface that contains the list of all part-based resources that are associated with the page.

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
<i>partResources</i> is <b>NULL</b>.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

If the page is not loaded when this method is called, this method finds the part-based resources that are associated with this page by parsing the relationships part of the page and returns them in the <i>partResources</i> parameter. If the page is loaded, this method traverses the page's object model to find the part-based resources and returns them in <i>partResources</i>.

The list of resource parts that are returned in the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a> interface is a snapshot of the document structure that is taken when the method is called. Changes made to the document after this call are not reflected in the <b>IXpsOMPartResources</b> interface after it is returned by this method. Likewise, changes made to the <b>IXpsOMPartResources</b> interface that is returned by this method will not be reflected in the document contents.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>