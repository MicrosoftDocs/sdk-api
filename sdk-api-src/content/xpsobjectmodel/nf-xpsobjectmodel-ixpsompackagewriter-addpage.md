---
UID: NF:xpsobjectmodel.IXpsOMPackageWriter.AddPage
title: IXpsOMPackageWriter::AddPage (xpsobjectmodel.h)
description: Writes a new FixedPage part to the currently open FixedDocument part in the package.
helpviewer_keywords: ["AddPage","AddPage method [XPS Documents and Packaging]","AddPage method [XPS Documents and Packaging]","IXpsOMPackageWriter interface","AddPage method [XPS Documents and Packaging]","IXpsOMPackageWriter3D interface","IXpsOMPackageWriter interface [XPS Documents and Packaging]","AddPage method","IXpsOMPackageWriter.AddPage","IXpsOMPackageWriter3D interface [XPS Documents and Packaging]","AddPage method","IXpsOMPackageWriter3D::AddPage","IXpsOMPackageWriter::AddPage","xps.ixpsompackagewriter_addpage","xpsobjectmodel/IXpsOMPackageWriter3D::AddPage","xpsobjectmodel/IXpsOMPackageWriter::AddPage"]
old-location: xps\ixpsompackagewriter_addpage.htm
tech.root: xps
ms.assetid: d7ea638d-f95c-4d72-8f55-cbb6a7d1ae8d
ms.date: 12/05/2018
ms.keywords: AddPage, AddPage method [XPS Documents and Packaging], AddPage method [XPS Documents and Packaging],IXpsOMPackageWriter interface, AddPage method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, IXpsOMPackageWriter interface [XPS Documents and Packaging],AddPage method, IXpsOMPackageWriter.AddPage, IXpsOMPackageWriter3D interface [XPS Documents and Packaging],AddPage method, IXpsOMPackageWriter3D::AddPage, IXpsOMPackageWriter::AddPage, xps.ixpsompackagewriter_addpage, xpsobjectmodel/IXpsOMPackageWriter3D::AddPage, xpsobjectmodel/IXpsOMPackageWriter::AddPage
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
 - IXpsOMPackageWriter::AddPage
 - xpsobjectmodel/IXpsOMPackageWriter::AddPage
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
 - IXpsOMPackageWriter.AddPage
 - IXpsOMPackageWriter3D.AddPage
---

# IXpsOMPackageWriter::AddPage


## -description

Writes a new FixedPage part to the currently open FixedDocument part in the package.

## -parameters

### -param page [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface whose page content is to be written to the currently open FixedDocument of the  package.

### -param advisoryPageDimensions [in]

The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a> structure that contains page dimensions.

Size is described in XPS units. There are 96 XPS units per inch.  For example, the dimensions of an 8.5" by 11.0" page are 816 by 1,056 XPS units.

### -param discardableResourceParts [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a> interface that contains a collection of the discardable resource parts.

### -param storyFragments [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a> interface that is to be  used for this page.

### -param pagePrintTicket [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface that contains the page-level print ticket for this page. See also Remarks.

### -param pageThumbnail [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface that contains the thumbnail image of this page.

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
<dt><b>XPS_E_MISSING_DISCARDCONTROL</b></dt>
</dl>
</td>
<td width="60%">
A page refers to discardable resources but does not specify a DiscardControl part name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_MISSING_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
This method was called before <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument">StartNewDocument</a>.

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
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

Call this method  after calling <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument">StartNewDocument</a>.

This method creates a new FixedPage  part in the package, copies the contents of the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface that is passed in the <i>page</i> parameter, and then closes the new FixedPage  part after the page has been written to the package.

If <i>pagePrintTicket</i> contains a <b>NULL</b> pointer and the package writer was created with interleaving set to <b>XPS_INTERLEAVING_ON</b>,  this method creates a blank page-level print ticket, if one does not already exist. Each time method is called with a <b>NULL</b> pointer in <i>pagePrintTicket</i>, it adds a relationship from the new page to the blank print ticket. This is done to provide more efficient streaming consumption of the package.

If <i>pagePrintTicket</i> contains a <b>NULL</b> pointer and the package writer was created with interleaving set to <b>XPS_INTERLEAVING_OFF</b>,  no blank print ticket is created.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>



<a href="/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsompackagewriter3d">IXpsOMPackageWriter3D</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection">IXpsOMPartUriCollection</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/dd464658(v=vs.85)">Using the IXpsOMPackageWriter Interface</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a>