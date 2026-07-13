---
UID: NN:xpsobjectmodel_2.IXpsDocumentPackageTarget3D
title: IXpsDocumentPackageTarget3D (xpsobjectmodel_2.h)
description: Provides methods for sending 3D content to XPS for printing.
helpviewer_keywords: ["IXpsDocumentPackageTarget3D","IXpsDocumentPackageTarget3D interface [XPS Documents and Packaging]","IXpsDocumentPackageTarget3D interface [XPS Documents and Packaging]","described","xps.ixpsdocumentpackagetarget3d","xpsobjectmodel_2/IXpsDocumentPackageTarget3D"]
old-location: xps\ixpsdocumentpackagetarget3d.htm
tech.root: xps
ms.assetid: 7273235D-EB74-4FB2-B471-FCFF71741BF6
ms.date: 12/05/2018
ms.keywords: IXpsDocumentPackageTarget3D, IXpsDocumentPackageTarget3D interface [XPS Documents and Packaging], IXpsDocumentPackageTarget3D interface [XPS Documents and Packaging],described, xps.ixpsdocumentpackagetarget3d, xpsobjectmodel_2/IXpsDocumentPackageTarget3D
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
 - IXpsDocumentPackageTarget3D
 - xpsobjectmodel_2/IXpsDocumentPackageTarget3D
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
 - IXpsDocumentPackageTarget3D
---

# IXpsDocumentPackageTarget3D interface

## -description

Provides methods for sending 3D content to XPS for printing.

## -inheritance

The <b>IXpsDocumentPackageTarget3D</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsDocumentPackageTarget3D</b> also has these types of members:

## -members

The <b>IXpsDocumentPackageTarget3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nf-xpsobjectmodel_2-ixpsdocumentpackagetarget3d-getxpsomfactory">GetXpsOMFactory</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a> object for the document package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nf-xpsobjectmodel_2-ixpsdocumentpackagetarget3d-getxpsompackagewriter3d">GetXpsOMPackageWriter3D</a>
</td>
<td align="left" width="63%">
Gets a new <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsompackagewriter3d">IXpsOMPackageWriter3D</a> object for the document package.

</td>
</tr>
</table>

## -members

The <b>IXpsDocumentPackageTarget3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nf-xpsobjectmodel_2-ixpsdocumentpackagetarget3d-getxpsomfactory">GetXpsOMFactory</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a> object for the document package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nf-xpsobjectmodel_2-ixpsdocumentpackagetarget3d-getxpsompackagewriter3d">GetXpsOMPackageWriter3D</a>
</td>
<td align="left" width="63%">
Gets a new <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsompackagewriter3d">IXpsOMPackageWriter3D</a> object for the document package.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsdocumentpackagetarget">IXpsDocumentPackageTarget</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>



<a href="/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsompackagewriter3d">IXpsOMPackageWriter3D</a>



<a href="/previous-versions/windows/apps/dn263137(v=win.10)">Supporting 3D printing</a>
