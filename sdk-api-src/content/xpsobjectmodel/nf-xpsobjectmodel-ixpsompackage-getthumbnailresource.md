---
UID: NF:xpsobjectmodel.IXpsOMPackage.GetThumbnailResource
title: IXpsOMPackage::GetThumbnailResource (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMImageResource interface of the thumbnail resource that is associated with the XPS package.
helpviewer_keywords: ["GetThumbnailResource","GetThumbnailResource method [XPS Documents and Packaging]","GetThumbnailResource method [XPS Documents and Packaging]","IXpsOMPackage interface","IXpsOMPackage interface [XPS Documents and Packaging]","GetThumbnailResource method","IXpsOMPackage.GetThumbnailResource","IXpsOMPackage::GetThumbnailResource","xps.ixpsompackage_getthumbnailresource","xpsobjectmodel/IXpsOMPackage::GetThumbnailResource"]
old-location: xps\ixpsompackage_getthumbnailresource.htm
tech.root: xps
ms.assetid: 44a692a4-de5d-4fa9-89e2-ad969042797a
ms.date: 12/05/2018
ms.keywords: GetThumbnailResource, GetThumbnailResource method [XPS Documents and Packaging], GetThumbnailResource method [XPS Documents and Packaging],IXpsOMPackage interface, IXpsOMPackage interface [XPS Documents and Packaging],GetThumbnailResource method, IXpsOMPackage.GetThumbnailResource, IXpsOMPackage::GetThumbnailResource, xps.ixpsompackage_getthumbnailresource, xpsobjectmodel/IXpsOMPackage::GetThumbnailResource
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
 - IXpsOMPackage::GetThumbnailResource
 - xpsobjectmodel/IXpsOMPackage::GetThumbnailResource
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
 - IXpsOMPackage.GetThumbnailResource
---

# IXpsOMPackage::GetThumbnailResource


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface of the thumbnail resource that is associated with the XPS package.

## -parameters

### -param imageResource [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface of the thumbnail resource that is associated with the XPS package. If the package does not have a thumbnail resource, a <b>NULL</b> pointer is returned.

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

## -remarks

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>