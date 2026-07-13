---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.CreatePackageWriterOnFile1
title: IXpsOMObjectFactory1::CreatePackageWriterOnFile1 (xpsobjectmodel_1.h)
description: Opens a file for writing the contents of an XPS OM to an XPS package of a specified type. This method produces a package writer for either an MSXPS document or an OpenXPS document.
helpviewer_keywords: ["CreatePackageWriterOnFile1","CreatePackageWriterOnFile1 method [XPS Documents and Packaging]","CreatePackageWriterOnFile1 method [XPS Documents and Packaging]","IXpsOMObjectFactory1 interface","FALSE","IXpsOMObjectFactory1 interface [XPS Documents and Packaging]","CreatePackageWriterOnFile1 method","IXpsOMObjectFactory1.CreatePackageWriterOnFile1","IXpsOMObjectFactory1::CreatePackageWriterOnFile1","TRUE","xps.ixpsomobjectfactory1_createpackagewriteronfile1","xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackageWriterOnFile1"]
old-location: xps\ixpsomobjectfactory1_createpackagewriteronfile1.htm
tech.root: xps
ms.assetid: 6ad569a1-8b7a-473c-8bce-ad1fd843ec29
ms.date: 12/05/2018
ms.keywords: CreatePackageWriterOnFile1, CreatePackageWriterOnFile1 method [XPS Documents and Packaging], CreatePackageWriterOnFile1 method [XPS Documents and Packaging],IXpsOMObjectFactory1 interface, FALSE, IXpsOMObjectFactory1 interface [XPS Documents and Packaging],CreatePackageWriterOnFile1 method, IXpsOMObjectFactory1.CreatePackageWriterOnFile1, IXpsOMObjectFactory1::CreatePackageWriterOnFile1, TRUE, xps.ixpsomobjectfactory1_createpackagewriteronfile1, xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackageWriterOnFile1
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
 - IXpsOMObjectFactory1::CreatePackageWriterOnFile1
 - xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackageWriterOnFile1
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
 - IXpsOMObjectFactory1.CreatePackageWriterOnFile1
---

# IXpsOMObjectFactory1::CreatePackageWriterOnFile1


## -description

Opens a file for writing the contents of an XPS OM to an XPS package of a specified type. This method produces a package writer for either an MSXPS document or an OpenXPS document.

## -parameters

### -param fileName

[in] The name of the file to be created.

### -param securityAttributes

[in, unique]    The <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure, which contains two separate but related  members:

<ul>
<li><b>lpSecurityDescriptor</b>: an optional security descriptor</li>
<li><b>bInheritHandle</b>:  a Boolean value that determines whether the returned handle can be inherited by child processes</li>
</ul>
If  <b>lpSecurityDescriptor</b> is <b>NULL</b>, the file or device associated with the returned handle is assigned a default security descriptor.

 For more information about <i>securityAttributes</i>, see <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

### -param flagsAndAttributes

[in]            Specifies the settings and attributes of the file to be created. For most files, the <b>FILE_ATTRIBUTE_NORMAL</b> value can be used.

See <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> for more information about this parameter.

### -param optimizeMarkupSize

[in] A Boolean value that  indicates whether the document markup will be optimized for size when the contents of the XPS OM are written to the XPS package.

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
The package writer will try to optimize the markup for minimum size.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The package writer will not try to perform any optimization.

</td>
</tr>
</table>

### -param interleaving

[in] Specifies whether the content of the XPS OM will be interleaved when it is written to the file.

### -param documentSequencePartName

[in] The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name of the document sequence in the new file.

### -param coreProperties

[in] The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a> interface that contains the core document properties to be given to the new file. This parameter can be set to <b>NULL</b>.

### -param packageThumbnail

[in] The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface that contains the thumbnail image to be assigned to the new file. This parameter can be set to <b>NULL</b>.

### -param documentSequencePrintTicket

[in] The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface that contains the package-level print ticket to be assigned to the new file. This parameter can be set to <b>NULL</b>.

### -param discardControlPartName

[in] The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the name of the discard control part. This parameter can be set to <b>NULL</b>.

### -param documentType

[in] Specifies the document type of the package writer. The value of this parameter cannot be XPS_DOCUMENT_TYPE_UNSPECIFIED.

### -param packageWriter

[out, retval]    A pointer to the new  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface created by this method.

## -returns

Possible values include, but are not limited to, the following. For information about XPS document API return values that are not listed here, see XPS Document Errors.

S_OK: The method succeeded and packageWriter was set correctly. 

E_INVALIDARG: The document type was not a valid XPS document format.

## -remarks

Use this method to produce a package writer for either an MSXPS document or an OpenXPS document. <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile">CreatePackageWriterOnFile</a>,  released in Windows 7, only creates XPS document files in the MSXPS format.

<h3><a id="Additional_References"></a><a id="additional_references"></a><a id="ADDITIONAL_REFERENCES"></a>Additional References</h3>
Additional References: Legacy method description

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1">IXpsOMObjectFactory1</a>