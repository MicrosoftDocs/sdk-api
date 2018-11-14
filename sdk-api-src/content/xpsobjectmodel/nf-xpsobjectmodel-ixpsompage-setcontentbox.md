---
UID: NF:xpsobjectmodel.IXpsOMPage.SetContentBox
title: IXpsOMPage::SetContentBox
author: windows-sdk-content
description: Sets the dimensions of the page's content box.
old-location: xps\ixpsompage_setcontentbox.htm
tech.root: printdocs
ms.assetid: 5262ce99-8112-4f4f-a173-5927341b4a2e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMPage interface [XPS Documents and Packaging],SetContentBox method, IXpsOMPage.SetContentBox, IXpsOMPage::SetContentBox, SetContentBox, SetContentBox method [XPS Documents and Packaging], SetContentBox method [XPS Documents and Packaging],IXpsOMPage interface, xps.ixpsompage_setcontentbox, xpsobjectmodel/IXpsOMPage::SetContentBox
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
 - IXpsOMPage.SetContentBox
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMPage.SetContentBox
: 
---

# IXpsOMPage::SetContentBox


## -description


Sets the dimensions of the page's content box.


## -parameters




### -param contentBox [in]

The dimensions of the page's content box.

<table>
<tr>
<th><i>contentBox</i> field</th>
<th>Valid values</th>
</tr>
<tr>
<td><i>contentBox.width</i></td>
<td>Greater than or equal to 0.0 and less than or equal to  (pageDimensions.width - contentBox.x).</td>
</tr>
<tr>
<td><i>contentBox.height</i></td>
<td>Greater than or equal to 0.0 and less than or equal to (pageDimensions.height - contentBox.y).</td>
</tr>
<tr>
<td><i>contentBox.x</i></td>
<td>Greater than or equal to 0.0 and less than pageDimensions.width.</td>
</tr>
<tr>
<td><i>contentBox.y</i></td>
<td>Greater than or equal to 0.0 and less than pageDimensions.height.</td>
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
<i>contentBox</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_CONTENT_BOX</b></dt>
</dl>
</td>
<td width="60%">
The rectangle specified by <i>contentBox</i> contains one or more values that are not valid.

</td>
</tr>
</table>
 




## -remarks



The content box specifies where ink appears on the page.

The content box dimensions are not checked against the page dimensions until the page is serialized.




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/e78a9ecb-b2e7-4295-a178-4a9936b0f27e">XPS_RECT</a>
 

 

