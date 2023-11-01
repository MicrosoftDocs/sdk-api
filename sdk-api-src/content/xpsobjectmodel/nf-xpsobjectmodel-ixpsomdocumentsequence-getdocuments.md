---
UID: NF:xpsobjectmodel.IXpsOMDocumentSequence.GetDocuments
title: IXpsOMDocumentSequence::GetDocuments (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMDocumentCollection interface, which contains the documents specified in the document sequence.
helpviewer_keywords: ["GetDocuments","GetDocuments method [XPS Documents and Packaging]","GetDocuments method [XPS Documents and Packaging]","IXpsOMDocumentSequence interface","IXpsOMDocumentSequence interface [XPS Documents and Packaging]","GetDocuments method","IXpsOMDocumentSequence.GetDocuments","IXpsOMDocumentSequence::GetDocuments","xps.ixpsomdocumentsequence_getdocuments","xpsobjectmodel/IXpsOMDocumentSequence::GetDocuments"]
old-location: xps\ixpsomdocumentsequence_getdocuments.htm
tech.root: xps
ms.assetid: d924e610-1142-4623-b64b-219558fb07d6
ms.date: 12/05/2018
ms.keywords: GetDocuments, GetDocuments method [XPS Documents and Packaging], GetDocuments method [XPS Documents and Packaging],IXpsOMDocumentSequence interface, IXpsOMDocumentSequence interface [XPS Documents and Packaging],GetDocuments method, IXpsOMDocumentSequence.GetDocuments, IXpsOMDocumentSequence::GetDocuments, xps.ixpsomdocumentsequence_getdocuments, xpsobjectmodel/IXpsOMDocumentSequence::GetDocuments
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
 - IXpsOMDocumentSequence::GetDocuments
 - xpsobjectmodel/IXpsOMDocumentSequence::GetDocuments
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
 - IXpsOMDocumentSequence.GetDocuments
---

# IXpsOMDocumentSequence::GetDocuments


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection">IXpsOMDocumentCollection</a> interface, which contains the documents specified in the document sequence.

## -parameters

### -param documents [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection">IXpsOMDocumentCollection</a> interface, which contains the documents specified in the document sequence. If the sequence does not have any documents, the <b>IXpsOMDocumentCollection</b> interface will be empty.

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
<i>documents</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

If the document sequence does not have any documents, the document collection that is returned in <i>documents</i> will be empty. To get  the number of documents in the collection, call the collection's <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentcollection-getcount">GetCount</a> method.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>