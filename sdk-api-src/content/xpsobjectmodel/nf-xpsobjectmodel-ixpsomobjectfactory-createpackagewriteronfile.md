---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePackageWriterOnFile
title: IXpsOMObjectFactory::CreatePackageWriterOnFile (xpsobjectmodel.h)
description: Opens a file for writing the contents of an XPS OM to an XPS package.
helpviewer_keywords: ["CreatePackageWriterOnFile","CreatePackageWriterOnFile method [XPS Documents and Packaging]","CreatePackageWriterOnFile method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","FALSE","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreatePackageWriterOnFile method","IXpsOMObjectFactory.CreatePackageWriterOnFile","IXpsOMObjectFactory::CreatePackageWriterOnFile","TRUE","xps.ixpsomobjectfactory_createpackagewriteronfile","xpsobjectmodel/IXpsOMObjectFactory::CreatePackageWriterOnFile"]
old-location: xps\ixpsomobjectfactory_createpackagewriteronfile.htm
tech.root: xps
ms.assetid: 67d081a6-ec10-4cd3-8f77-b7653aef27a1
ms.date: 12/05/2018
ms.keywords: CreatePackageWriterOnFile, CreatePackageWriterOnFile method [XPS Documents and Packaging], CreatePackageWriterOnFile method [XPS Documents and Packaging],IXpsOMObjectFactory interface, FALSE, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePackageWriterOnFile method, IXpsOMObjectFactory.CreatePackageWriterOnFile, IXpsOMObjectFactory::CreatePackageWriterOnFile, TRUE, xps.ixpsomobjectfactory_createpackagewriteronfile, xpsobjectmodel/IXpsOMObjectFactory::CreatePackageWriterOnFile
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
 - IXpsOMObjectFactory::CreatePackageWriterOnFile
 - xpsobjectmodel/IXpsOMObjectFactory::CreatePackageWriterOnFile
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
 - IXpsOMObjectFactory.CreatePackageWriterOnFile
---

# IXpsOMObjectFactory::CreatePackageWriterOnFile


## -description

Opens a file for writing the contents of an XPS OM to an XPS package.

## -parameters

### -param fileName [in]

The name of the file to be created.

### -param securityAttributes [in]

The <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure, which contains two separate but related  members:

<ul>
<li><b>lpSecurityDescriptor</b>: an optional security descriptor</li>
<li><b>bInheritHandle</b>:  a Boolean value that determines whether the returned handle can be inherited by child processes</li>
</ul>
If  <b>lpSecurityDescriptor</b> is <b>NULL</b>, the file or device associated with the returned handle is assigned a default security descriptor.

 For more information about <i>securityAttributes</i>, see <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

### -param flagsAndAttributes [in]

Specifies the settings and attributes of the file to be created. For most files, the <b>FILE_ATTRIBUTE_NORMAL</b> value can be used.

See <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> for more information about this parameter.

### -param optimizeMarkupSize [in]

A Boolean value that  indicates whether the document markup will be optimized for size when the contents of the XPS OM are written to the XPS package.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The package writer will try to optimize the markup for minimum size.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The package writer will not try to perform any optimization.

</td>
</tr>
</table>

### -param interleaving [in]

Specifies whether the content of the XPS OM will be interleaved when it is written to the file.

### -param documentSequencePartName [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name of the document sequence in the new file.

### -param coreProperties [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a> interface that contains the core document properties to be given to the new file. This parameter can be set to <b>NULL</b>.

### -param packageThumbnail [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface that contains the thumbnail image to be assigned to the new file. This parameter can be set to <b>NULL</b>.

### -param documentSequencePrintTicket [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface that contains the package-level print ticket to be assigned to the new file. This parameter can be set to <b>NULL</b>.

### -param discardControlPartName [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the name of the discard control part. This parameter can be set to <b>NULL</b>.

### -param packageWriter [out, retval]

A pointer to the new  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface created by this method.

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
<i>filename</i>, <i>documentSequencePartName</i>,  or   <i>packageWriter</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>coreProperties</i>,  <i>documentSequencePrintTicket</i>, or <i>packageThumbnail</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

 The file is opened and initialized and the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface that is returned is then used to write content types, package relationships, core properties, document sequence resources, and document sequence relationships.

  

If <i>documentSequencePrintTicket</i> is set to  <b>NULL</b> and the value of <i>interleaving</i> is <b>XPS_INTERLEAVING_ON</b>,  this method creates a blank job-level print ticket and adds a relationship to the blank print ticket. This is done to provide more efficient streaming consumption of the package.

If <i>documentSequencePrintTicket</i> is set to <b>NULL</b> and the value of <i>interleaving</i> is <b>XPS_INTERLEAVING_OFF</b>,  no blank print ticket is created.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>