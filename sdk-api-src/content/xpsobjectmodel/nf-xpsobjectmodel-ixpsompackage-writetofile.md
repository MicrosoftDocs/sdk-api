---
UID: NF:xpsobjectmodel.IXpsOMPackage.WriteToFile
title: IXpsOMPackage::WriteToFile (xpsobjectmodel.h)
description: Writes the XPS package to a specified file.
helpviewer_keywords: ["FALSE","IXpsOMPackage interface [XPS Documents and Packaging]","WriteToFile method","IXpsOMPackage.WriteToFile","IXpsOMPackage::WriteToFile","TRUE","WriteToFile","WriteToFile method [XPS Documents and Packaging]","WriteToFile method [XPS Documents and Packaging]","IXpsOMPackage interface","xps.ixpsompackage_writetofile","xpsobjectmodel/IXpsOMPackage::WriteToFile"]
old-location: xps\ixpsompackage_writetofile.htm
tech.root: xps
ms.assetid: 89accde7-989e-4a87-b96e-e47cc6c6954a
ms.date: 12/05/2018
ms.keywords: FALSE, IXpsOMPackage interface [XPS Documents and Packaging],WriteToFile method, IXpsOMPackage.WriteToFile, IXpsOMPackage::WriteToFile, TRUE, WriteToFile, WriteToFile method [XPS Documents and Packaging], WriteToFile method [XPS Documents and Packaging],IXpsOMPackage interface, xps.ixpsompackage_writetofile, xpsobjectmodel/IXpsOMPackage::WriteToFile
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
 - IXpsOMPackage::WriteToFile
 - xpsobjectmodel/IXpsOMPackage::WriteToFile
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
 - IXpsOMPackage.WriteToFile
---

# IXpsOMPackage::WriteToFile


## -description

Writes the XPS package to a specified file.

## -parameters

### -param fileName [in]

The name of the file to be created. This parameter must not be <b>NULL</b>.

### -param securityAttributes [in]

The <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure, which contains two distinct but related data members:

<ul>
<li><b>lpSecurityDescriptor</b>: an optional security descriptor</li>
<li><b>bInheritHandle</b>:  a Boolean value that determines whether the returned handle can be inherited by child processes</li>
</ul>
If  <b>lpSecurityDescriptor</b> is <b>NULL</b>, the file or device that is associated with the returned handle will be assigned a default security descriptor. 

For more information about the <i>securityAttributes</i> parameter, refer to <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

### -param flagsAndAttributes [in]

Specifies the settings and attributes of the file to be  created. For most files, a value of <b>FILE_ATTRIBUTE_NORMAL</b> can be used. 


For more information about the <i>flagsAndAttributes</i> parameter, refer to <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

### -param optimizeMarkupSize [in]

A Boolean value that  indicates whether the document markup is to be optimized for size when it is written to the file.

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
The package writer will attempt to optimize the markup for minimum size.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The package writer will not attempt any optimization.

</td>
</tr>
</table>

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
<i>fileName</i> is <b>NULL</b>.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

The <i>optimizeMarkupSize</i> value determines whether the markup inside the individual document parts is to be optimized. It has  no effect on how the parts are interleaved.

<div class="alert"><b>Note</b>  Writing an XPS OM to a file does not automatically create a thumbnail for the XPS document. To create a thumbnail of the XPS document, use the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator">IXpsOMThumbnailGenerator</a> interface.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>