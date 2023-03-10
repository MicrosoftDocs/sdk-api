---
UID: NN:xpsobjectmodel_2.IXpsOMPackageWriter3D
title: IXpsOMPackageWriter3D (xpsobjectmodel_2.h)
description: Contains methods that support model textures and print ticket.
helpviewer_keywords: ["IXpsOMPackageWriter3D","IXpsOMPackageWriter3D interface [XPS Documents and Packaging]","IXpsOMPackageWriter3D interface [XPS Documents and Packaging]","described","xps.ixpsompackagewriter3d","xpsobjectmodel_2/IXpsOMPackageWriter3D"]
old-location: xps\ixpsompackagewriter3d.htm
tech.root: xps
ms.assetid: 2F3E0529-7E2B-4BCD-AE8F-D0F3259D1A48
ms.date: 12/05/2018
ms.keywords: IXpsOMPackageWriter3D, IXpsOMPackageWriter3D interface [XPS Documents and Packaging], IXpsOMPackageWriter3D interface [XPS Documents and Packaging],described, xps.ixpsompackagewriter3d, xpsobjectmodel_2/IXpsOMPackageWriter3D
req.header: xpsobjectmodel_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel_1.idl; XpsObjectModel_2.idl
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
 - IXpsOMPackageWriter3D
 - xpsobjectmodel_2/IXpsOMPackageWriter3D
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsObjectModel_2.h
api_name:
 - IXpsOMPackageWriter3D
---

# IXpsOMPackageWriter3D interface

## -description

Contains methods that support model textures and print ticket.

## -inheritance

The <b>IXpsOMPackageWriter3D</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>. <b>IXpsOMPackageWriter3D</b> also has these types of members:

## -members

The <b>IXpsOMPackageWriter3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nf-xpsobjectmodel_2-ixpsompackagewriter3d-addmodeltexture">AddModelTexture</a>
</td>
<td align="left" width="63%">
Creates a new 3D model texture from the specified texture part and stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage">IXpsOMPackageWriter::AddPage</a>
</td>
<td align="left" width="63%">
Writes a new FixedPage part to the currently open FixedDocument part in the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addresource">IXpsOMPackageWriter::AddResource</a>
</td>
<td align="left" width="63%">
Creates a new part resource in the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close">IXpsOMPackageWriter::Close</a>
</td>
<td align="left" width="63%">
Closes any open parts of the package, then closes the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-isclosed">IXpsOMPackageWriter::IsClosed</a>
</td>
<td align="left" width="63%">
Gets the status of the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument">IXpsOMPackageWriter::StartNewDocument</a>
</td>
<td align="left" width="63%">
Opens and initializes a new FixedDocument in the FixedDocumentSequence of the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nf-xpsobjectmodel_2-ixpsompackagewriter3d-setmodelprintticket">SetModelPrintTicket</a>
</td>
<td align="left" width="63%">
Creates a print ticket with the specified part.

</td>
</tr>
</table>

## -members

The <b>IXpsOMPackageWriter3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nf-xpsobjectmodel_2-ixpsompackagewriter3d-addmodeltexture">AddModelTexture</a>
</td>
<td align="left" width="63%">
Creates a new 3D model texture from the specified texture part and stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage">IXpsOMPackageWriter::AddPage</a>
</td>
<td align="left" width="63%">
Writes a new FixedPage part to the currently open FixedDocument part in the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addresource">IXpsOMPackageWriter::AddResource</a>
</td>
<td align="left" width="63%">
Creates a new part resource in the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close">IXpsOMPackageWriter::Close</a>
</td>
<td align="left" width="63%">
Closes any open parts of the package, then closes the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-isclosed">IXpsOMPackageWriter::IsClosed</a>
</td>
<td align="left" width="63%">
Gets the status of the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument">IXpsOMPackageWriter::StartNewDocument</a>
</td>
<td align="left" width="63%">
Opens and initializes a new FixedDocument in the FixedDocumentSequence of the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nf-xpsobjectmodel_2-ixpsompackagewriter3d-setmodelprintticket">SetModelPrintTicket</a>
</td>
<td align="left" width="63%">
Creates a print ticket with the specified part.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsdocumentpackagetarget">IXpsDocumentPackageTarget</a>



<a href="/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsdocumentpackagetarget3d">IXpsDocumentPackageTarget3D</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>



<a href="/previous-versions/windows/apps/dn263137(v=win.10)">Supporting 3D printing</a>
