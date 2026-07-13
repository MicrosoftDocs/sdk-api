---
UID: NF:xpsobjectmodel.IXpsOMPackage.WriteToStream
title: IXpsOMPackage::WriteToStream (xpsobjectmodel.h)
description: Writes the XPS package to a specified stream.
helpviewer_keywords: ["FALSE","IXpsOMPackage interface [XPS Documents and Packaging]","WriteToStream method","IXpsOMPackage.WriteToStream","IXpsOMPackage::WriteToStream","TRUE","WriteToStream","WriteToStream method [XPS Documents and Packaging]","WriteToStream method [XPS Documents and Packaging]","IXpsOMPackage interface","xps.ixpsompackage_writetostream","xpsobjectmodel/IXpsOMPackage::WriteToStream"]
old-location: xps\ixpsompackage_writetostream.htm
tech.root: xps
ms.assetid: 5b729ac6-3f0e-4f24-b3f6-4b6d26844df1
ms.date: 12/05/2018
ms.keywords: FALSE, IXpsOMPackage interface [XPS Documents and Packaging],WriteToStream method, IXpsOMPackage.WriteToStream, IXpsOMPackage::WriteToStream, TRUE, WriteToStream, WriteToStream method [XPS Documents and Packaging], WriteToStream method [XPS Documents and Packaging],IXpsOMPackage interface, xps.ixpsompackage_writetostream, xpsobjectmodel/IXpsOMPackage::WriteToStream
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
 - IXpsOMPackage::WriteToStream
 - xpsobjectmodel/IXpsOMPackage::WriteToStream
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
 - IXpsOMPackage.WriteToStream
---

# IXpsOMPackage::WriteToStream


## -description

Writes the XPS package to a specified stream.

## -parameters

### -param stream [in]

The stream that receives the serialized contents of the package. This parameter must not be <b>NULL</b>.

### -param optimizeMarkupSize [in]

A Boolean value that  indicates whether the document markup is to be optimized for size when it is written to the stream.

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
<i>stream</i> is <b>NULL</b>.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

The <i>optimizeMarkupSize</i> value determines whether the markup inside the individual document parts is to be optimized. It has  no effect on how the parts are interleaved.

<div class="alert"><b>Note</b>  Writing an XPS OM to a stream does not automatically create a thumbnail for the XPS document. To create a thumbnail of the XPS document, use the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator">IXpsOMThumbnailGenerator</a> interface.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage">IXpsOMPackage</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>