---
UID: NF:xpsobjectmodel.IXpsOMThumbnailGenerator.GenerateThumbnail
title: IXpsOMThumbnailGenerator::GenerateThumbnail (xpsobjectmodel.h)
description: Generates a thumbnail image of a page.
helpviewer_keywords: ["GenerateThumbnail","GenerateThumbnail method [XPS Documents and Packaging]","GenerateThumbnail method [XPS Documents and Packaging]","IXpsOMThumbnailGenerator interface","IXpsOMThumbnailGenerator interface [XPS Documents and Packaging]","GenerateThumbnail method","IXpsOMThumbnailGenerator.GenerateThumbnail","IXpsOMThumbnailGenerator::GenerateThumbnail","xps.ixpsomthumbnailgenerator_generatethumbnail","xpsobjectmodel/IXpsOMThumbnailGenerator::GenerateThumbnail"]
old-location: xps\ixpsomthumbnailgenerator_generatethumbnail.htm
tech.root: xps
ms.assetid: 8a2431f0-50e5-43a9-8940-62d9babad297
ms.date: 12/05/2018
ms.keywords: GenerateThumbnail, GenerateThumbnail method [XPS Documents and Packaging], GenerateThumbnail method [XPS Documents and Packaging],IXpsOMThumbnailGenerator interface, IXpsOMThumbnailGenerator interface [XPS Documents and Packaging],GenerateThumbnail method, IXpsOMThumbnailGenerator.GenerateThumbnail, IXpsOMThumbnailGenerator::GenerateThumbnail, xps.ixpsomthumbnailgenerator_generatethumbnail, xpsobjectmodel/IXpsOMThumbnailGenerator::GenerateThumbnail
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - IXpsOMThumbnailGenerator::GenerateThumbnail
 - xpsobjectmodel/IXpsOMThumbnailGenerator::GenerateThumbnail
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
 - IXpsOMThumbnailGenerator.GenerateThumbnail
---

# IXpsOMThumbnailGenerator::GenerateThumbnail


## -description

Generates a thumbnail image of a page.

## -parameters

### -param page [in]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface that contains the page for which the thumbnail image will be created.

### -param thumbnailType [in]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type">XPS_IMAGE_TYPE</a> value that specifies the type of thumbnail image to create.

### -param thumbnailSize [in]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_thumbnail_size">XPS_THUMBNAIL_SIZE</a> value that specifies the image size of the thumbnail to create.

### -param imageResourcePartName [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the name of the new thumbnail image part.

### -param imageResource [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface that contains the thumbnail image created by this method.

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
<i>page</i>, <i>imageResourcePartName</i>, or <i>imageResource</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the following parameters contains a value that is not valid:

<ul>
<li><i>thumbnailType</i>: The image type must be PNG (<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type">XPS_IMAGE_TYPE_PNG</a>) or JPEG (<b>XPS_IMAGE_TYPE_JPEG</b>)</li>
<li><i>thumbnailSize</i>: <i>thumbnailSize</i> must be a member of  <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_thumbnail_size">XPS_THUMBNAIL_SIZE</a>
</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator">IXpsOMThumbnailGenerator</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type">XPS_IMAGE_TYPE</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_thumbnail_size">XPS_THUMBNAIL_SIZE</a>