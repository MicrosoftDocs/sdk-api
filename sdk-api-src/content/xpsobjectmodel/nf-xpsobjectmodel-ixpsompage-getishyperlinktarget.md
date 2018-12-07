---
UID: NF:xpsobjectmodel.IXpsOMPage.GetIsHyperlinkTarget
title: IXpsOMPage::GetIsHyperlinkTarget
author: windows-sdk-content
description: Gets a Boolean value that indicates whether the page is the target of a hyperlink.
old-location: xps\ixpsompage_getishyperlinktarget.htm
tech.root: printdocs
ms.assetid: 172636d5-c375-4552-97a8-d874b6aa4843
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetIsHyperlinkTarget, GetIsHyperlinkTarget method [XPS Documents and Packaging], GetIsHyperlinkTarget method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetIsHyperlinkTarget method, IXpsOMPage.GetIsHyperlinkTarget, IXpsOMPage::GetIsHyperlinkTarget, xps.ixpsompage_getishyperlinktarget, xpsobjectmodel/IXpsOMPage::GetIsHyperlinkTarget
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMPage.GetIsHyperlinkTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<i>isHyperlinkTarget</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

