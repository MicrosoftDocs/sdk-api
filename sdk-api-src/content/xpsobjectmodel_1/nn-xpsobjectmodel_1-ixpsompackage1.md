---
UID: NN:xpsobjectmodel_1.IXpsOMPackage1
title: IXpsOMPackage1 (xpsobjectmodel_1.h)
description: Inherits from IXpsOMPackage.
helpviewer_keywords: ["IXpsOMPackage1","IXpsOMPackage1 interface [XPS Documents and Packaging]","IXpsOMPackage1 interface [XPS Documents and Packaging]","described","xps.ixpsompackage1","xpsobjectmodel_1/IXpsOMPackage1"]
old-location: xps\ixpsompackage1.htm
tech.root: xps
ms.assetid: 455b7f0b-ade4-4e00-bd9d-836335a7982e
ms.date: 12/05/2018
ms.keywords: IXpsOMPackage1, IXpsOMPackage1 interface [XPS Documents and Packaging], IXpsOMPackage1 interface [XPS Documents and Packaging],described, xps.ixpsompackage1, xpsobjectmodel_1/IXpsOMPackage1
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: None
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMPackage1
 - xpsobjectmodel_1/IXpsOMPackage1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - none
 - none.dll
api_name:
 - IXpsOMPackage1
---

# IXpsOMPackage1 interface

## -description

Inherits from IXpsOMPackage. 

Provides support for:

Detecting the format/type of an XPS package loaded in the XPS OM.

Saving an in-memory XPS OM package to an MSXPS or OpenXPS package byte stream or file.

## -inheritance

The <b>IXpsOMPackage1</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a>. <b>IXpsOMPackage1</b> also has these types of members:

## -members

The <b>IXpsOMPackage1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype">IXpsOMPackage1::GetDocumentType</a>
</td>
<td align="left" width="63%">
Gets the document type of the data that was used to initialize this package. This method is used to determine whether a document is the XPS or OpenXPS type. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316975(v=vs.85)">XPS Documents</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsompackage1-writetofile1">IXpsOMPackage1::WriteToFile1</a>
</td>
<td align="left" width="63%">
Writes an XPS OM to a file as an XPS package of a specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsompackage1-writetostream1">IXpsOMPackage1::WriteToStream1</a>
</td>
<td align="left" width="63%">
Writes an XPS OM to a stream as an XPS package of a specified type.

</td>
</tr>
</table>

## -members

The <b>IXpsOMPackage1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype">IXpsOMPackage1::GetDocumentType</a>
</td>
<td align="left" width="63%">
Gets the document type of the data that was used to initialize this package. This method is used to determine whether a document is the XPS or OpenXPS type. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316975(v=vs.85)">XPS Documents</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsompackage1-writetofile1">IXpsOMPackage1::WriteToFile1</a>
</td>
<td align="left" width="63%">
Writes an XPS OM to a file as an XPS package of a specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsompackage1-writetostream1">IXpsOMPackage1::WriteToStream1</a>
</td>
<td align="left" width="63%">
Writes an XPS OM to a stream as an XPS package of a specified type.

</td>
</tr>
</table>

## -remarks

<h3><a id="Additional_References"></a><a id="additional_references"></a><a id="ADDITIONAL_REFERENCES"></a>Additional References</h3>
The base interface is defined and documented in Windows 7 SDK.

[IXpsOMPackage interface](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a>
