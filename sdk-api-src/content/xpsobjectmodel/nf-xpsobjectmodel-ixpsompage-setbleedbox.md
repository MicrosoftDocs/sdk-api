---
UID: NF:xpsobjectmodel.IXpsOMPage.SetBleedBox
title: IXpsOMPage::SetBleedBox (xpsobjectmodel.h)
description: Sets the dimensions of the page's bleed box.
helpviewer_keywords: ["IXpsOMPage interface [XPS Documents and Packaging]","SetBleedBox method","IXpsOMPage.SetBleedBox","IXpsOMPage::SetBleedBox","SetBleedBox","SetBleedBox method [XPS Documents and Packaging]","SetBleedBox method [XPS Documents and Packaging]","IXpsOMPage interface","bleedBox.height","bleedBox.width","bleedBox.x","bleedBox.y","xps.ixpsompage_setbleedbox","xpsobjectmodel/IXpsOMPage::SetBleedBox"]
old-location: xps\ixpsompage_setbleedbox.htm
tech.root: xps
ms.assetid: 947313e1-6c95-4751-997f-d5172acaa5d5
ms.date: 12/05/2018
ms.keywords: IXpsOMPage interface [XPS Documents and Packaging],SetBleedBox method, IXpsOMPage.SetBleedBox, IXpsOMPage::SetBleedBox, SetBleedBox, SetBleedBox method [XPS Documents and Packaging], SetBleedBox method [XPS Documents and Packaging],IXpsOMPage interface, bleedBox.height, bleedBox.width, bleedBox.x, bleedBox.y, xps.ixpsompage_setbleedbox, xpsobjectmodel/IXpsOMPage::SetBleedBox
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
 - IXpsOMPage::SetBleedBox
 - xpsobjectmodel/IXpsOMPage::SetBleedBox
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
 - IXpsOMPage.SetBleedBox
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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_rect">XPS_RECT</a>