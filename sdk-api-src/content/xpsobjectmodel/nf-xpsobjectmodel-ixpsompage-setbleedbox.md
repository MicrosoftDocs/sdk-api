---
UID: NF:xpsobjectmodel.IXpsOMPage.SetBleedBox
title: IXpsOMPage::SetBleedBox
author: windows-sdk-content
description: Sets the dimensions of the page's bleed box.
old-location: xps\ixpsompage_setbleedbox.htm
tech.root: printdocs
ms.assetid: 947313e1-6c95-4751-997f-d5172acaa5d5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXpsOMPage interface [XPS Documents and Packaging],SetBleedBox method, IXpsOMPage.SetBleedBox, IXpsOMPage::SetBleedBox, SetBleedBox, SetBleedBox method [XPS Documents and Packaging], SetBleedBox method [XPS Documents and Packaging],IXpsOMPage interface, bleedBox.height, bleedBox.width, bleedBox.x, bleedBox.y, xps.ixpsompage_setbleedbox, xpsobjectmodel/IXpsOMPage::SetBleedBox
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
 - IXpsOMPage.SetBleedBox
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
- IXpsOMPage.SetBleedBox
: 
---

# IXpsOMPage::SetBleedBox


## -description


Sets the dimensions of the page's bleed box.


## -parameters




### -param bleedBox [in]

The dimensions of the page's bleed box. This parameter must not be <b>NULL</b>.

A valid bleed box has the following properties:



####### x)) ≤ value )



####### y)) ≤ value )



###### 0)



###### 0)


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
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_BLEED_BOX</b></dt>
</dl>
</td>
<td width="60%">
The rectangle described by <i>bleedBox</i> contains one or more values that are not valid.

</td>
</tr>
</table>
 




## -remarks



The bleed box dimensions are not checked against the page dimensions until the page is serialized.




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/e78a9ecb-b2e7-4295-a178-4a9936b0f27e">XPS_RECT</a>
 

 

