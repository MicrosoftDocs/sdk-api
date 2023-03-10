---
UID: NN:xpsobjectmodel_1.IXpsOMPage1
title: IXpsOMPage1 (xpsobjectmodel_1.h)
description: Inherits from IXpsOMPage.
helpviewer_keywords: ["IXpsOMPage1","IXpsOMPage1 interface [XPS Documents and Packaging]","IXpsOMPage1 interface [XPS Documents and Packaging]","described","xps.ixpsompage1","xpsobjectmodel_1/IXpsOMPage1"]
old-location: xps\ixpsompage1.htm
tech.root: xps
ms.assetid: 4f4ec7d9-da77-4d34-89aa-a73250c0e610
ms.date: 12/05/2018
ms.keywords: IXpsOMPage1, IXpsOMPage1 interface [XPS Documents and Packaging], IXpsOMPage1 interface [XPS Documents and Packaging],described, xps.ixpsompage1, xpsobjectmodel_1/IXpsOMPage1
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
 - IXpsOMPage1
 - xpsobjectmodel_1/IXpsOMPage1
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
 - IXpsOMPage1
---

# IXpsOMPage1 interface

## -description

Inherits from IXpsOMPage. 

Provides support for:

Detecting the type of XPS FixedPage markup which this page was loaded from.

Serializing page objects to markup of the requested type - MSXPS or OpenXps.

## -inheritance

The <b>IXpsOMPage1</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>. <b>IXpsOMPage1</b> also has these types of members:

## -members

The <b>IXpsOMPage1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype">IXpsOMPage1::GetDocumentType</a>
</td>
<td align="left" width="63%">
Gets the type of FixedPage markup that was used to initialize this page. This method is used to determine whether a document is the XPS or OpenXPS type. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316975(v=vs.85)">XPS Documents</a>.

</td>
</tr>
</table>

## -members

The <b>IXpsOMPage1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype">IXpsOMPage1::GetDocumentType</a>
</td>
<td align="left" width="63%">
Gets the type of FixedPage markup that was used to initialize this page. This method is used to determine whether a document is the XPS or OpenXPS type. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316975(v=vs.85)">XPS Documents</a>.

</td>
</tr>
</table>

## -remarks

<h3><a id="Additional_References"></a><a id="additional_references"></a><a id="ADDITIONAL_REFERENCES"></a>Additional References</h3>
The base interface is defined and documented in Windows 7 SDK.

[IXpsOMPage interface](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>
