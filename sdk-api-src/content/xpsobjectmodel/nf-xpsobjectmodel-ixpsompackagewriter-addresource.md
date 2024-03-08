---
UID: NF:xpsobjectmodel.IXpsOMPackageWriter.AddResource
title: IXpsOMPackageWriter::AddResource (xpsobjectmodel.h)
description: Creates a new part resource in the package.
helpviewer_keywords: ["AddResource","AddResource method [XPS Documents and Packaging]","AddResource method [XPS Documents and Packaging]","IXpsOMPackageWriter interface","AddResource method [XPS Documents and Packaging]","IXpsOMPackageWriter3D interface","IXpsOMPackageWriter interface [XPS Documents and Packaging]","AddResource method","IXpsOMPackageWriter.AddResource","IXpsOMPackageWriter3D interface [XPS Documents and Packaging]","AddResource method","IXpsOMPackageWriter3D::AddResource","IXpsOMPackageWriter::AddResource","xps.ixpsompackagewriter_addresource","xpsobjectmodel/IXpsOMPackageWriter3D::AddResource","xpsobjectmodel/IXpsOMPackageWriter::AddResource"]
old-location: xps\ixpsompackagewriter_addresource.htm
tech.root: xps
ms.assetid: eb81efb8-f3cd-448d-ab60-34acf13db4cd
ms.date: 12/05/2018
ms.keywords: AddResource, AddResource method [XPS Documents and Packaging], AddResource method [XPS Documents and Packaging],IXpsOMPackageWriter interface, AddResource method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, IXpsOMPackageWriter interface [XPS Documents and Packaging],AddResource method, IXpsOMPackageWriter.AddResource, IXpsOMPackageWriter3D interface [XPS Documents and Packaging],AddResource method, IXpsOMPackageWriter3D::AddResource, IXpsOMPackageWriter::AddResource, xps.ixpsompackagewriter_addresource, xpsobjectmodel/IXpsOMPackageWriter3D::AddResource, xpsobjectmodel/IXpsOMPackageWriter::AddResource
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
 - IXpsOMPackageWriter::AddResource
 - xpsobjectmodel/IXpsOMPackageWriter::AddResource
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
 - IXpsOMPackageWriter.AddResource
 - IXpsOMPackageWriter3D.AddResource
---

# IXpsOMPackageWriter::AddResource


## -description

Creates a new part resource in the package.

## -parameters

### -param resource [in]

The <a href="/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a> interface of the part resource that will be added as a new part in the package. See Remarks for the types of resources that may be passed in this parameter.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A resource with the same name as the resource that is referenced by <i>resource</i> has already been added to the stream or there is no  relationship that includes the resource that is referenced by <i>resource</i>.

After <b>E_INVALIDARG</b> is returned, the stream or file is no longer valid and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close">Close</a> will return  <b>XPS_E_UNAVAILABLE_PACKAGE</b>.

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

This method creates a new part in the document package that corresponds to <i>resource</i>, adds the contents of  <i>resource</i> to the new part, and then closes the new  part.

If this method returns an error, the package writer is no longer usable.

The <i>resource</i> parameter must be one of the following:<ul>
<li>The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface of a font resource that is used in the current page or a page that has already been added.</li>
<li>The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface of an image resource that is used in the current page or  a page that has already been added.</li>
<li>The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface of  color profile resource that is used in the current page or a page that has already been added.</li>
<li>The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a> interface of a story fragments resource that is used in the current page or a page that has already been added.</li>
<li>The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a> interface of a document structure resource that is used in the current document or a document that has already been added.</li>
<li>The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresource">IXpsOMSignatureBlockResource</a> interface of a signature block resource that is used in the current document or a document that has already been added.</li>
</ul>


This method returns an error if <i>resource</i> contains one of the following:<ul>
<li>The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface of a remote resource dictionary.</li>
<li>The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface of a print ticket.</li>
<li>The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface of a thumbnail image.</li>
</ul>


This method returns an error when <i>resource</i> references a resource that has the same name as  a resource that  has already been added to the stream or for which there is no existing relationship.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>



<a href="/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsompackagewriter3d">IXpsOMPackageWriter3D</a>



<a href="/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/dd464658(v=vs.85)">Using the IXpsOMPackageWriter Interface</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>