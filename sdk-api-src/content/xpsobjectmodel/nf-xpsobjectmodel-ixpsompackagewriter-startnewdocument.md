---
UID: NF:xpsobjectmodel.IXpsOMPackageWriter.StartNewDocument
title: IXpsOMPackageWriter::StartNewDocument (xpsobjectmodel.h)
author: windows-sdk-content
description: Opens and initializes a new FixedDocument in the FixedDocumentSequence of the package.
old-location: xps\ixpsompackagewriter_startnewdocument.htm
tech.root: printdocs
ms.assetid: da5fdbcd-ff3c-403a-a565-1590908cf333
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMPackageWriter interface [XPS Documents and Packaging],StartNewDocument method, IXpsOMPackageWriter.StartNewDocument, IXpsOMPackageWriter3D interface [XPS Documents and Packaging],StartNewDocument method, IXpsOMPackageWriter3D::StartNewDocument, IXpsOMPackageWriter::StartNewDocument, StartNewDocument, StartNewDocument method [XPS Documents and Packaging], StartNewDocument method [XPS Documents and Packaging],IXpsOMPackageWriter interface, StartNewDocument method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, xps.ixpsompackagewriter_startnewdocument, xpsobjectmodel/IXpsOMPackageWriter3D::StartNewDocument, xpsobjectmodel/IXpsOMPackageWriter::StartNewDocument
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPackageWriter::StartNewDocument


## -description


Opens and initializes a new FixedDocument in the FixedDocumentSequence of the package.


## -parameters




### -param documentPartName [in]

A pointer to an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name of the new document.


### -param documentPrintTicket [in]

A pointer to an <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface that contains the document-level print ticket.  If there is no document-level print ticket for this package, this parameter can be set to <b>NULL</b>. See also Remarks.


### -param documentStructure [in]

A pointer to an <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface that contains the initial document structure resource, if the resource is available; if it is not available, this parameter can be set to <b>NULL</b>.


### -param signatureBlockResources [in]

A pointer to an <a href="https://msdn.microsoft.com/681bdb9c-69dd-4bf6-a4b3-c490f7a0363e">IXpsOMSignatureBlockResourceCollection</a> interface that contains a collection of digital signatures to be attached to the document. If there are no digital signatures to be attached, this parameter can be set to <b>NULL</b>.


### -param restrictedFonts [in]

A pointer to an <a href="https://msdn.microsoft.com/05fe9700-19e6-4e63-9693-cfa4b019f643">IXpsOMPartUriCollection</a> interface that contains the  fonts that must have restricted font relationships written for them. The font data are not written until <a href="https://msdn.microsoft.com/eb81efb8-f3cd-448d-ab60-34acf13db4cd">AddResource</a> or <a href="https://msdn.microsoft.com/916fbdaa-bef7-4a6f-9259-47347b47dc27">Close</a> is called.

If the document does not contain any  restricted fonts, this parameter can be set to <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
 

This method calls the <a href="https://msdn.microsoft.com/77df9cb2-757e-4b07-9c1c-73af0df4702f">Packaging</a> API. For information about the Packaging API return values, see <a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>.




## -remarks



This method must be called before <a href="https://msdn.microsoft.com/d7ea638d-f95c-4d72-8f55-cbb6a7d1ae8d">AddPage</a> can be called to write the contents of an <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface.

Immediately after the <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> interface has been instantiated, the package contains only an empty Fixed Document Sequence part.  The first time this method is called,  a  FixedDocument part is added to the Fixed Document Sequence part and the <a href="https://msdn.microsoft.com/d7ea638d-f95c-4d72-8f55-cbb6a7d1ae8d">AddPage</a> method will add pages to that FixedDocument part. Each time this method is called after the first time, the current FixedDocument part is closed, and a new FixedDocument part is opened and added to the Fixed Document Sequence part.  All subsequent calls to the <b>AddPage</b>  method add pages to the most recently opened FixedDocument part. This interface does not support adding pages to closed FixedDocument parts.

If <i>documentPrintTicket</i> contains a <b>NULL</b> pointer and the package writer was created with interleaving set to <b>XPS_INTERLEAVING_ON</b>,  this method creates a blank document-level print ticket, if one does not already exist. Each time this method is called with a <b>NULL</b> pointer in <i>documentPrintTicket</i>, it adds a relationship from the new document to the blank print ticket. This is done to provide more efficient streaming consumption of the package.

If <i>documentPrintTicket</i> contains a <b>NULL</b> pointer and the package writer was created with interleaving set to <b>XPS_INTERLEAVING_OFF</b>,  no blank print ticket is created.

<div class="alert"><b>Note</b>  Creating a new document in the package  does not automatically create a thumbnail for the XPS document. To create a thumbnail of the XPS document, use the <a href="https://msdn.microsoft.com/cac794c0-bea2-417e-880f-15838f718ba7">IXpsOMThumbnailGenerator</a> interface.</div>
<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a>



<a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a>



<a href="https://msdn.microsoft.com/2F3E0529-7E2B-4BCD-AE8F-D0F3259D1A48">IXpsOMPackageWriter3D</a>



<a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a>



<a href="https://msdn.microsoft.com/681bdb9c-69dd-4bf6-a4b3-c490f7a0363e">IXpsOMSignatureBlockResourceCollection</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/eff1ab1e-2205-4f5c-9e32-199e073f5dbf">Using the IXpsOMPackageWriter Interface</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

