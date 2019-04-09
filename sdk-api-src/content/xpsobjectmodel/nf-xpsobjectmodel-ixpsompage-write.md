---
UID: NF:xpsobjectmodel.IXpsOMPage.Write
title: IXpsOMPage::Write (xpsobjectmodel.h)
author: windows-sdk-content
description: Writes the page to the specified stream.
old-location: xps\ixpsompage_write.htm
tech.root: printdocs
ms.assetid: ab586c7d-69e6-4ad7-93f1-3e1437c04856
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FALSE, IXpsOMPage interface [XPS Documents and Packaging],Write method, IXpsOMPage.Write, IXpsOMPage::Write, TRUE, Write, Write method [XPS Documents and Packaging], Write method [XPS Documents and Packaging],IXpsOMPage interface, xps.ixpsompage_write, xpsobjectmodel/IXpsOMPage::Write
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
 - IXpsOMPage.Write
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPage::Write


## -description


Writes the page to the specified stream.


## -parameters




### -param stream [in]

The stream that receives the serialized contents of the page.


### -param optimizeMarkupSize [in]

A Boolean value that  indicates whether the document markup of the page is to be optimized for size when the page is written to the stream. 

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
The package writer will attempt to optimize the markup for minimum size when writing the page to the stream.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The package writer will not attempt any optimization when writing the page to the stream.

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
 




## -remarks



To examine the XPS markup of a page before it is written to an XPS package, an application can call the <b>Write</b> method to write the page's contents to a stream. The application can then read that stream to examine the XPS markup as it would be serialized when it is written to the XPS package.

The XPS markup that is  written to the stream by this method contains the page markup but none of the page's resources.




## -see-also




<a href="https://msdn.microsoft.com/c1d33800-d2f1-4942-92fa-e115f524c23c">ISequentialStream</a>



<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

