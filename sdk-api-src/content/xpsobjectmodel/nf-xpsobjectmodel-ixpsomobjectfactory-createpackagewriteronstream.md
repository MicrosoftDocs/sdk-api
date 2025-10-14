---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePackageWriterOnStream
title: IXpsOMObjectFactory::CreatePackageWriterOnStream (xpsobjectmodel.h)
description: Opens a stream for writing the contents of an XPS OM to an XPS package.
helpviewer_keywords: ["CreatePackageWriterOnStream","CreatePackageWriterOnStream method [XPS Documents and Packaging]","CreatePackageWriterOnStream method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","FALSE","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreatePackageWriterOnStream method","IXpsOMObjectFactory.CreatePackageWriterOnStream","IXpsOMObjectFactory::CreatePackageWriterOnStream","TRUE","xps.ixpsomobjectfactory_createpackagewriteronstream","xpsobjectmodel/IXpsOMObjectFactory::CreatePackageWriterOnStream"]
old-location: xps\ixpsomobjectfactory_createpackagewriteronstream.htm
tech.root: xps
ms.assetid: 77f432e3-7b6a-426f-8673-06dbf3038443
ms.date: 12/05/2018
ms.keywords: CreatePackageWriterOnStream, CreatePackageWriterOnStream method [XPS Documents and Packaging], CreatePackageWriterOnStream method [XPS Documents and Packaging],IXpsOMObjectFactory interface, FALSE, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePackageWriterOnStream method, IXpsOMObjectFactory.CreatePackageWriterOnStream, IXpsOMObjectFactory::CreatePackageWriterOnStream, TRUE, xps.ixpsomobjectfactory_createpackagewriteronstream, xpsobjectmodel/IXpsOMObjectFactory::CreatePackageWriterOnStream
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
 - IXpsOMObjectFactory::CreatePackageWriterOnStream
 - xpsobjectmodel/IXpsOMObjectFactory::CreatePackageWriterOnStream
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
 - IXpsOMObjectFactory.CreatePackageWriterOnStream
---

# IXpsOMObjectFactory::CreatePackageWriterOnStream


## -description

Opens a stream for writing the contents of an XPS OM to an XPS package.

## -parameters

### -param outputStream [in]

The stream to be used for writing.

### -param optimizeMarkupSize [in]

A Boolean value that  indicates whether the document markup will be optimized for size when the document is written to the stream.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
When writing to the stream, the package writer will attempt to optimize the markup for minimum size.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
When writing to the package, the package writer will not attempt any optimization.

</td>
</tr>
</table>

### -param interleaving [in]

Specifies whether the content of the XPS OM will be interleaved when it is written to the stream.

### -param documentSequencePartName [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name of the document sequence in the new file.

### -param coreProperties [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a> interface that contains the core document properties to be given to the new file. This parameter can be set to <b>NULL</b>.

### -param packageThumbnail [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface that contains the thumbnail image to be assigned to the new file.  This parameter can be set to <b>NULL</b>.

### -param documentSequencePrintTicket [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface that contains the package-level print ticket to be assigned to the new file.  This parameter can be set to <b>NULL</b>.

### -param discardControlPartName [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the name of the discard control part.  This parameter can be set to <b>NULL</b>.

### -param packageWriter [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface created by this method.

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
<i>outputStream</i>, <i>documentSequencePartName</i>, or <i>packageWriter</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>coreProperties</i>,  <i>documentSequencePrintTicket</i> or <i>packageThumbnail</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

The stream is opened and initialized, and then the returned <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface  is used to write content types, package relationships, core properties, document sequence resources, and document sequence relationships.

If <i>documentSequencePrintTicket</i> is set to <b>NULL</b> and the value of <i>interleaving</i> is <b>XPS_INTERLEAVING_ON</b>,  this method creates a blank job-level print ticket and adds a relationship to the blank print ticket. This is done to provide more efficient streaming consumption of the package.

If <i>documentSequencePrintTicket</i> is set to  <b>NULL</b> and the value of <i>interleaving</i> is <b>XPS_INTERLEAVING_OFF</b>,  no blank print ticket is created.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>