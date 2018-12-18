---
UID: NF:xpsobjectmodel.IXpsOMPage.GetBleedBox
title: IXpsOMPage::GetBleedBox
author: windows-sdk-content
description: Gets the dimensions of the page's bleed box.
old-location: xps\ixpsompage_getbleedbox.htm
tech.root: printdocs
ms.assetid: 2ce82a0e-b01c-4c1e-8907-31f51dc51f10
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBleedBox, GetBleedBox method [XPS Documents and Packaging], GetBleedBox method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetBleedBox method, IXpsOMPage.GetBleedBox, IXpsOMPage::GetBleedBox, xps.ixpsompage_getbleedbox, xpsobjectmodel/IXpsOMPage::GetBleedBox
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
 - IXpsOMPage.GetBleedBox
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPage::GetBleedBox


## -description


Gets the dimensions of the page's bleed box.


## -parameters




### -param bleedBox [out, retval]

The dimensions of the bleed box.


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
<i>bleedBox</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The default bleed box of a page is:

<table>
<tr>
<th>
<a href="https://msdn.microsoft.com/e78a9ecb-b2e7-4295-a178-4a9936b0f27e">XPS_RECT</a> field</th>
<th>Default value</th>
</tr>
<tr>
<td>x</td>
<td>0</td>
</tr>
<tr>
<td>y</td>
<td>0</td>
</tr>
<tr>
<td>width</td>
<td>pageDimension.width</td>
</tr>
<tr>
<td>height</td>
<td>pageDimension.height</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/e78a9ecb-b2e7-4295-a178-4a9936b0f27e">XPS_RECT</a>
 

 

