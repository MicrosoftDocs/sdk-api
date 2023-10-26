---
UID: NF:xpsobjectmodel.IXpsOMPageReference.SetAdvisoryPageDimensions
title: IXpsOMPageReference::SetAdvisoryPageDimensions (xpsobjectmodel.h)
description: Sets the suggested dimensions of the page.
helpviewer_keywords: ["IXpsOMPageReference interface [XPS Documents and Packaging]","SetAdvisoryPageDimensions method","IXpsOMPageReference.SetAdvisoryPageDimensions","IXpsOMPageReference::SetAdvisoryPageDimensions","SetAdvisoryPageDimensions","SetAdvisoryPageDimensions method [XPS Documents and Packaging]","SetAdvisoryPageDimensions method [XPS Documents and Packaging]","IXpsOMPageReference interface","xps.ixpsompagereference_setadvisorypagedimensions","xpsobjectmodel/IXpsOMPageReference::SetAdvisoryPageDimensions"]
old-location: xps\ixpsompagereference_setadvisorypagedimensions.htm
tech.root: xps
ms.assetid: 8286fd78-a7d8-4bf4-9b08-b93e19abccf9
ms.date: 12/05/2018
ms.keywords: IXpsOMPageReference interface [XPS Documents and Packaging],SetAdvisoryPageDimensions method, IXpsOMPageReference.SetAdvisoryPageDimensions, IXpsOMPageReference::SetAdvisoryPageDimensions, SetAdvisoryPageDimensions, SetAdvisoryPageDimensions method [XPS Documents and Packaging], SetAdvisoryPageDimensions method [XPS Documents and Packaging],IXpsOMPageReference interface, xps.ixpsompagereference_setadvisorypagedimensions, xpsobjectmodel/IXpsOMPageReference::SetAdvisoryPageDimensions
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
 - IXpsOMPageReference::SetAdvisoryPageDimensions
 - xpsobjectmodel/IXpsOMPageReference::SetAdvisoryPageDimensions
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
 - IXpsOMPageReference.SetAdvisoryPageDimensions
---

# IXpsOMPageReference::SetAdvisoryPageDimensions


## -description

Sets the suggested dimensions of the page.

## -parameters

### -param pageDimensions [in]

The suggested dimensions to be set for the page.

The <b>height</b> and <b>width</b> members  must have the value of –1.0 or a value that is greater than or equal to +1.0.

Size is described in XPS units. There are 96 XPS units per inch.  For example, the dimensions of an 8.5" by 11.0" page are 816 by 1,056 XPS units.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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
Either <i>pageDimensions</i> is <b>NULL</b> or a field in the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a> structure that is referenced by <i>pageDimensions</i> contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_PAGE_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The advisory page size described in <i>pageDimensions</i> was not valid. The <b>height</b> and <b>width</b> members of <i>pageDimensions</i>  must have the value of –1.0 or a value that is greater than or equal to +1.0.

</td>
</tr>
</table>

## -remarks

The <b>height</b> and <b>width</b>  members of the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a> structure that is referenced by <i>pageDimensions</i> must have values that are greater than or equal to +1.0, if those fields' values are to be set, or –1.0 if not. For example, if an advisory  dimension were to be set just for the page width,  <i>pageDimensions.width</i> would have the desired value and <i>pageDimensions.height</i> would have the value of –1.0.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a>