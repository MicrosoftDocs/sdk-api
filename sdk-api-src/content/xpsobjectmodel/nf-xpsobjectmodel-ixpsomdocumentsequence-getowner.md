---
UID: NF:xpsobjectmodel.IXpsOMDocumentSequence.GetOwner
title: IXpsOMDocumentSequence::GetOwner (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMPackage interface that contains the document sequence.
helpviewer_keywords: ["GetOwner","GetOwner method [XPS Documents and Packaging]","GetOwner method [XPS Documents and Packaging]","IXpsOMDocumentSequence interface","IXpsOMDocumentSequence interface [XPS Documents and Packaging]","GetOwner method","IXpsOMDocumentSequence.GetOwner","IXpsOMDocumentSequence::GetOwner","xps.ixpsomdocumentsequence_getowner","xpsobjectmodel/IXpsOMDocumentSequence::GetOwner"]
old-location: xps\ixpsomdocumentsequence_getowner.htm
tech.root: xps
ms.assetid: c5c59e70-d7b5-42cf-a979-6da4899203ba
ms.date: 12/05/2018
ms.keywords: GetOwner, GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging],IXpsOMDocumentSequence interface, IXpsOMDocumentSequence interface [XPS Documents and Packaging],GetOwner method, IXpsOMDocumentSequence.GetOwner, IXpsOMDocumentSequence::GetOwner, xps.ixpsomdocumentsequence_getowner, xpsobjectmodel/IXpsOMDocumentSequence::GetOwner
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
 - IXpsOMDocumentSequence::GetOwner
 - xpsobjectmodel/IXpsOMDocumentSequence::GetOwner
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
 - IXpsOMDocumentSequence.GetOwner
---

# IXpsOMDocumentSequence::GetOwner


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a> interface that contains the document sequence.

## -parameters

### -param package [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a> interface that contains the document sequence.  If the document sequence does not belong to a package, a <b>NULL</b> pointer is returned.

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
<i>package</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>