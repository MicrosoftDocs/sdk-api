---
UID: NF:xpsobjectmodel.IXpsOMPackage.WriteToStream
title: IXpsOMPackage::WriteToStream method
author: windows-driver-content
description: Writes the XPS package to a specified stream.
old-location: xps\ixpsompackage_writetostream.htm
old-project: printdocs
ms.assetid: 5b729ac6-3f0e-4f24-b3f6-4b6d26844df1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FALSE, IXpsOMPackage, IXpsOMPackage interface [XPS Documents and Packaging], WriteToStream method, IXpsOMPackage::WriteToStream, TRUE, WriteToStream method [XPS Documents and Packaging], WriteToStream method [XPS Documents and Packaging], IXpsOMPackage interface, WriteToStream,IXpsOMPackage.WriteToStream, xps.ixpsompackage_writetostream, xpsobjectmodel/IXpsOMPackage::WriteToStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMPackage.WriteToStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPackage::WriteToStream method


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
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The package writer will attempt to optimize the markup for minimum size.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The package writer will not attempt any optimization.

</td>
</tr>
</table>
 


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>stream</i> is <b>NULL</b>.

</td>
</tr>
</table>
 

This method calls the <a href="https://msdn.microsoft.com/77df9cb2-757e-4b07-9c1c-73af0df4702f">Packaging</a> API. For information about the Packaging API return values, see <a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>.




## -remarks



The <i>optimizeMarkupSize</i> value determines whether the markup inside the individual document parts is to be optimized. It has  no effect on how the parts are interleaved.

<div class="alert"><b>Note</b>  Writing an XPS OM to a stream does not automatically create a thumbnail for the XPS document. To create a thumbnail of the XPS document, use the <a href="https://msdn.microsoft.com/cac794c0-bea2-417e-880f-15838f718ba7">IXpsOMThumbnailGenerator</a> interface.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c1d33800-d2f1-4942-92fa-e115f524c23c">ISequentialStream</a>



<a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

