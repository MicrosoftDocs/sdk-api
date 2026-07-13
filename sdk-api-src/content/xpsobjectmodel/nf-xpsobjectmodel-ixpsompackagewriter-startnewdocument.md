---
UID: NF:xpsobjectmodel.IXpsOMPackageWriter.StartNewDocument
title: IXpsOMPackageWriter::StartNewDocument (xpsobjectmodel.h)
description: Opens and initializes a new FixedDocument in the FixedDocumentSequence of the package.
helpviewer_keywords: ["IXpsOMPackageWriter interface [XPS Documents and Packaging]","StartNewDocument method","IXpsOMPackageWriter.StartNewDocument","IXpsOMPackageWriter3D interface [XPS Documents and Packaging]","StartNewDocument method","IXpsOMPackageWriter3D::StartNewDocument","IXpsOMPackageWriter::StartNewDocument","StartNewDocument","StartNewDocument method [XPS Documents and Packaging]","StartNewDocument method [XPS Documents and Packaging]","IXpsOMPackageWriter interface","StartNewDocument method [XPS Documents and Packaging]","IXpsOMPackageWriter3D interface","xps.ixpsompackagewriter_startnewdocument","xpsobjectmodel/IXpsOMPackageWriter3D::StartNewDocument","xpsobjectmodel/IXpsOMPackageWriter::StartNewDocument"]
old-location: xps\ixpsompackagewriter_startnewdocument.htm
tech.root: xps
ms.assetid: da5fdbcd-ff3c-403a-a565-1590908cf333
ms.date: 12/05/2018
ms.keywords: IXpsOMPackageWriter interface [XPS Documents and Packaging],StartNewDocument method, IXpsOMPackageWriter.StartNewDocument, IXpsOMPackageWriter3D interface [XPS Documents and Packaging],StartNewDocument method, IXpsOMPackageWriter3D::StartNewDocument, IXpsOMPackageWriter::StartNewDocument, StartNewDocument, StartNewDocument method [XPS Documents and Packaging], StartNewDocument method [XPS Documents and Packaging],IXpsOMPackageWriter interface, StartNewDocument method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, xps.ixpsompackagewriter_startnewdocument, xpsobjectmodel/IXpsOMPackageWriter3D::StartNewDocument, xpsobjectmodel/IXpsOMPackageWriter::StartNewDocument
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
 - IXpsOMPackageWriter::StartNewDocument
 - xpsobjectmodel/IXpsOMPackageWriter::StartNewDocument
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
 - IXpsOMPackageWriter.StartNewDocument
 - IXpsOMPackageWriter3D.StartNewDocument
---

# IXpsOMPackageWriter::StartNewDocument


## -description

Opens and initializes a new FixedDocument in the FixedDocumentSequence of the package.

## -parameters

### -param documentPartName [in]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name of the new document.

### -param documentPrintTicket [in]

A pointer to an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface that contains the document-level print ticket.  If there is no document-level print ticket for this package, this parameter can be set to <b>NULL</b>. See also Remarks.

### -param documentStructure [in]

A pointer to an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a> interface that contains the initial document structure resource, if the resource is available; if it is not available, this parameter can be set to <b>NULL</b>.

### -param signatureBlockResources [in]

A pointer to an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection">IXpsOMSignatureBlockResourceCollection</a> interface that contains a collection of digital signatures to be attached to the document. If there are no digital signatures to be attached, this parameter can be set to <b>NULL</b>.

### -param restrictedFonts [in]

A pointer to an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a> interface that contains the  fonts that must have restricted font relationships written for them. The font data are not written until <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addresource">AddResource</a> or <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close">Close</a> is called.

If the document does not contain any  restricted fonts, this parameter can be set to <b>NULL</b>.

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
<dt><b>XPS_E_UNAVAILABLE_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
A severe error occurred and the contents of the XPS OM might be unrecoverable. Some components of the XPS OM might still be usable but only after they have been verified. Because the state of the XPS OM cannot be predicted after this error is returned, all components of the XPS OM should be released and discarded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</b></dt>
</dl>
</td>
<td width="60%">
The restricted font collection passed in <i>restrictedFonts</i> contains an unrestricted font.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

This method must be called before <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage">AddPage</a> can be called to write the contents of an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface.

Immediately after the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface has been instantiated, the package contains only an empty Fixed Document Sequence part.  The first time this method is called,  a  FixedDocument part is added to the Fixed Document Sequence part and the <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage">AddPage</a> method will add pages to that FixedDocument part. Each time this method is called after the first time, the current FixedDocument part is closed, and a new FixedDocument part is opened and added to the Fixed Document Sequence part.  All subsequent calls to the <b>AddPage</b>  method add pages to the most recently opened FixedDocument part. This interface does not support adding pages to closed FixedDocument parts.

If <i>documentPrintTicket</i> contains a <b>NULL</b> pointer and the package writer was created with interleaving set to <b>XPS_INTERLEAVING_ON</b>,  this method creates a blank document-level print ticket, if one does not already exist. Each time this method is called with a <b>NULL</b> pointer in <i>documentPrintTicket</i>, it adds a relationship from the new document to the blank print ticket. This is done to provide more efficient streaming consumption of the package.

If <i>documentPrintTicket</i> contains a <b>NULL</b> pointer and the package writer was created with interleaving set to <b>XPS_INTERLEAVING_OFF</b>,  no blank print ticket is created.

<div class="alert"><b>Note</b>  Creating a new document in the package  does not automatically create a thumbnail for the XPS document. To create a thumbnail of the XPS document, use the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator">IXpsOMThumbnailGenerator</a> interface.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>



<a href="/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsompackagewriter3d">IXpsOMPackageWriter3D</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection">IXpsOMSignatureBlockResourceCollection</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/dd464658(v=vs.85)">Using the IXpsOMPackageWriter Interface</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>