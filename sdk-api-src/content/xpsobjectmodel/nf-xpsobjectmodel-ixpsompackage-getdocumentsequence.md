---
UID: NF:xpsobjectmodel.IXpsOMPackage.GetDocumentSequence
title: IXpsOMPackage::GetDocumentSequence (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMDocumentSequence interface that contains the document sequence of the XPS package.
helpviewer_keywords: ["GetDocumentSequence","GetDocumentSequence method [XPS Documents and Packaging]","GetDocumentSequence method [XPS Documents and Packaging]","IXpsOMPackage interface","IXpsOMPackage interface [XPS Documents and Packaging]","GetDocumentSequence method","IXpsOMPackage.GetDocumentSequence","IXpsOMPackage::GetDocumentSequence","xps.ixpsompackage_getdocumentsequence","xpsobjectmodel/IXpsOMPackage::GetDocumentSequence"]
old-location: xps\ixpsompackage_getdocumentsequence.htm
tech.root: xps
ms.assetid: 30789376-1ac8-41ae-9c4d-e3d2d0715016
ms.date: 12/05/2018
ms.keywords: GetDocumentSequence, GetDocumentSequence method [XPS Documents and Packaging], GetDocumentSequence method [XPS Documents and Packaging],IXpsOMPackage interface, IXpsOMPackage interface [XPS Documents and Packaging],GetDocumentSequence method, IXpsOMPackage.GetDocumentSequence, IXpsOMPackage::GetDocumentSequence, xps.ixpsompackage_getdocumentsequence, xpsobjectmodel/IXpsOMPackage::GetDocumentSequence
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
 - IXpsOMPackage::GetDocumentSequence
 - xpsobjectmodel/IXpsOMPackage::GetDocumentSequence
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
 - IXpsOMPackage.GetDocumentSequence
---

# IXpsOMPackage::GetDocumentSequence


## -description

Gets a pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a> interface that contains the document sequence of the XPS package.

## -parameters

### -param documentSequence [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a> interface that contains the document sequence of the  XPS package. If an <b>IXpsOMDocumentSequence</b> interface has not been set, a <b>NULL</b> pointer is returned.

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
<i>documentSequence</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>