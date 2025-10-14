---
UID: NF:xpsobjectmodel.IXpsOMPage.Write
title: IXpsOMPage::Write (xpsobjectmodel.h)
description: Writes the page to the specified stream.
helpviewer_keywords: ["FALSE","IXpsOMPage interface [XPS Documents and Packaging]","Write method","IXpsOMPage.Write","IXpsOMPage::Write","TRUE","Write","Write method [XPS Documents and Packaging]","Write method [XPS Documents and Packaging]","IXpsOMPage interface","xps.ixpsompage_write","xpsobjectmodel/IXpsOMPage::Write"]
old-location: xps\ixpsompage_write.htm
tech.root: xps
ms.assetid: ab586c7d-69e6-4ad7-93f1-3e1437c04856
ms.date: 12/05/2018
ms.keywords: FALSE, IXpsOMPage interface [XPS Documents and Packaging],Write method, IXpsOMPage.Write, IXpsOMPage::Write, TRUE, Write, Write method [XPS Documents and Packaging], Write method [XPS Documents and Packaging],IXpsOMPage interface, xps.ixpsompage_write, xpsobjectmodel/IXpsOMPage::Write
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
 - IXpsOMPage::Write
 - xpsobjectmodel/IXpsOMPage::Write
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
 - IXpsOMPage.Write
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
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The package writer will attempt to optimize the markup for minimum size when writing the page to the stream.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The package writer will not attempt any optimization when writing the page to the stream.

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

## -remarks

To examine the XPS markup of a page before it is written to an XPS package, an application can call the <b>Write</b> method to write the page's contents to a stream. The application can then read that stream to examine the XPS markup as it would be serialized when it is written to the XPS package.

The XPS markup that is  written to the stream by this method contains the page markup but none of the page's resources.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>