---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.CreatePackageWriterOnStream1
title: IXpsOMObjectFactory1::CreatePackageWriterOnStream1 (xpsobjectmodel_1.h)
description: Opens a stream for writing the contents of an XPS OM to an XPS package of a specified type.
helpviewer_keywords: ["CreatePackageWriterOnStream1","CreatePackageWriterOnStream1 method [XPS Documents and Packaging]","CreatePackageWriterOnStream1 method [XPS Documents and Packaging]","IXpsOMObjectFactory1 interface","FALSE","IXpsOMObjectFactory1 interface [XPS Documents and Packaging]","CreatePackageWriterOnStream1 method","IXpsOMObjectFactory1.CreatePackageWriterOnStream1","IXpsOMObjectFactory1::CreatePackageWriterOnStream1","TRUE","xps.ixpsomobjectfactory1_createpackagewriteronstream1","xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackageWriterOnStream1"]
old-location: xps\ixpsomobjectfactory1_createpackagewriteronstream1.htm
tech.root: xps
ms.assetid: ce948f17-689a-4430-8152-20fbecaf6ee9
ms.date: 12/05/2018
ms.keywords: CreatePackageWriterOnStream1, CreatePackageWriterOnStream1 method [XPS Documents and Packaging], CreatePackageWriterOnStream1 method [XPS Documents and Packaging],IXpsOMObjectFactory1 interface, FALSE, IXpsOMObjectFactory1 interface [XPS Documents and Packaging],CreatePackageWriterOnStream1 method, IXpsOMObjectFactory1.CreatePackageWriterOnStream1, IXpsOMObjectFactory1::CreatePackageWriterOnStream1, TRUE, xps.ixpsomobjectfactory1_createpackagewriteronstream1, xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackageWriterOnStream1
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
 - IXpsOMObjectFactory1::CreatePackageWriterOnStream1
 - xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackageWriterOnStream1
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
 - IXpsOMObjectFactory1.CreatePackageWriterOnStream1
---

# IXpsOMObjectFactory1::CreatePackageWriterOnStream1


## -description

Opens a stream for writing the contents of an XPS OM to an XPS package of a specified type.

## -parameters

### -param outputStream

[in] The stream to be used for writing.

### -param optimizeMarkupSize

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

### -param interleaving

[in] Specifies whether the content of the XPS OM will be interleaved when it is written to the stream.

### -param documentSequencePartName

[in] The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name of the document sequence in the new file.

### -param coreProperties

[in] The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a> interface that contains the core document properties to be given to the new file. This parameter can be set to <b>NULL</b>.

### -param packageThumbnail

[in] The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface that contains the thumbnail image to be assigned to the new file.  This parameter can be set to <b>NULL</b>.

### -param documentSequencePrintTicket

[in] The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface that contains the package-level print ticket to be assigned to the new file.  This parameter can be set to <b>NULL</b>.

### -param discardControlPartName

[in] The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the name of the discard control part.  This parameter can be set to <b>NULL</b>.

### -param documentType

[in] The document type of the package writer. The value of this parameter cannot be XPS_DOCUMENT_TYPE_UNSPECIFIED.

### -param packageWriter

[out, retval]    A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface created by this method.

## -returns

Possible values include, but are not limited to, the following. For information about XPS document API return values that are not listed here, see XPS Document Errors.

S_OK: The method succeeded and packageWriter was set correctly. 

E_INVALIDARG: The document type was not a valid XPS document format.

## -remarks

Use this method to produce a package writer for either an MSXPS document or an OpenXPS document. <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream">CreatePackageWriterOnStream</a>,  released in Windows 7, only creates XPS document files in the MSXPS format.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1">IXpsOMObjectFactory1</a>