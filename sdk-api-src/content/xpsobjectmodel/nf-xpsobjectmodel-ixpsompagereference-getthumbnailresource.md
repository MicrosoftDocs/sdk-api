---
UID: NF:xpsobjectmodel.IXpsOMPageReference.GetThumbnailResource
title: IXpsOMPageReference::GetThumbnailResource (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMImageResource interface of the thumbnail image resource that is associated with the page.
helpviewer_keywords: ["GetThumbnailResource","GetThumbnailResource method [XPS Documents and Packaging]","GetThumbnailResource method [XPS Documents and Packaging]","IXpsOMPageReference interface","IXpsOMPageReference interface [XPS Documents and Packaging]","GetThumbnailResource method","IXpsOMPageReference.GetThumbnailResource","IXpsOMPageReference::GetThumbnailResource","xps.ixpsompagereference_getthumbnailresource","xpsobjectmodel/IXpsOMPageReference::GetThumbnailResource"]
old-location: xps\ixpsompagereference_getthumbnailresource.htm
tech.root: xps
ms.assetid: ec9cc698-892f-4216-b491-cabdfa60deaa
ms.date: 12/05/2018
ms.keywords: GetThumbnailResource, GetThumbnailResource method [XPS Documents and Packaging], GetThumbnailResource method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],GetThumbnailResource method, IXpsOMPageReference.GetThumbnailResource, IXpsOMPageReference::GetThumbnailResource, xps.ixpsompagereference_getthumbnailresource, xpsobjectmodel/IXpsOMPageReference::GetThumbnailResource
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
 - IXpsOMPageReference::GetThumbnailResource
 - xpsobjectmodel/IXpsOMPageReference::GetThumbnailResource
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
 - IXpsOMPageReference.GetThumbnailResource
---

# IXpsOMPageReference::GetThumbnailResource


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface of the  thumbnail image resource that is associated with the page.

## -parameters

### -param imageResource [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface of the  thumbnail image resource that is associated with the page.  If no thumbnail image resource has been assigned to the page, a <b>NULL</b> pointer is returned.

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
<i>imageResource</i> is <b>NULL</b>.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

The thumbnail image is a small, visual representation of the page's  contents.

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>