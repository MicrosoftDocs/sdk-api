---
UID: NF:xpsobjectmodel.IXpsOMPage.GetIsHyperlinkTarget
title: IXpsOMPage::GetIsHyperlinkTarget (xpsobjectmodel.h)
description: Gets a Boolean value that indicates whether the page is the target of a hyperlink.
helpviewer_keywords: ["GetIsHyperlinkTarget","GetIsHyperlinkTarget method [XPS Documents and Packaging]","GetIsHyperlinkTarget method [XPS Documents and Packaging]","IXpsOMPage interface","IXpsOMPage interface [XPS Documents and Packaging]","GetIsHyperlinkTarget method","IXpsOMPage.GetIsHyperlinkTarget","IXpsOMPage::GetIsHyperlinkTarget","xps.ixpsompage_getishyperlinktarget","xpsobjectmodel/IXpsOMPage::GetIsHyperlinkTarget"]
old-location: xps\ixpsompage_getishyperlinktarget.htm
tech.root: xps
ms.assetid: 172636d5-c375-4552-97a8-d874b6aa4843
ms.date: 12/05/2018
ms.keywords: GetIsHyperlinkTarget, GetIsHyperlinkTarget method [XPS Documents and Packaging], GetIsHyperlinkTarget method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetIsHyperlinkTarget method, IXpsOMPage.GetIsHyperlinkTarget, IXpsOMPage::GetIsHyperlinkTarget, xps.ixpsompage_getishyperlinktarget, xpsobjectmodel/IXpsOMPage::GetIsHyperlinkTarget
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
 - IXpsOMPage::GetIsHyperlinkTarget
 - xpsobjectmodel/IXpsOMPage::GetIsHyperlinkTarget
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
 - IXpsOMPage.GetIsHyperlinkTarget
---

# IXpsOMPage::GetIsHyperlinkTarget


## -description

Gets a Boolean value that indicates whether the page is the target of a hyperlink.

## -parameters

### -param isHyperlinkTarget [out, retval]

A Boolean value that indicates whether the page is the target of a hyperlink. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The page is the target of a hyperlink.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The page is not the target of a hyperlink.

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
<i>isHyperlinkTarget</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>