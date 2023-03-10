---
UID: NF:msinkaut.IInkDisp.CreateStroke
title: IInkDisp::CreateStroke (msinkaut.h)
description: Creates an IInkStrokeDisp object from an array of packet data input values.
helpviewer_keywords: ["116c5746-61ad-4a47-a5e3-4675af87b0f1","CreateStroke","CreateStroke method [Tablet PC]","CreateStroke method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","CreateStroke method","IInkDisp.CreateStroke","IInkDisp::CreateStroke","msinkaut/IInkDisp::CreateStroke","tablet.inkdisp_createstroke"]
old-location: tablet\inkdisp_createstroke.htm
tech.root: tablet
ms.assetid: 116c5746-61ad-4a47-a5e3-4675af87b0f1
ms.date: 12/05/2018
ms.keywords: 116c5746-61ad-4a47-a5e3-4675af87b0f1, CreateStroke, CreateStroke method [Tablet PC], CreateStroke method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],CreateStroke method, IInkDisp.CreateStroke, IInkDisp::CreateStroke, msinkaut/IInkDisp::CreateStroke, tablet.inkdisp_createstroke
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDisp::CreateStroke
 - msinkaut/IInkDisp::CreateStroke
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkDisp.CreateStroke
---

# IInkDisp::CreateStroke


## -description

Creates an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object from an array of packet data input values.

## -parameters

### -param PacketData [in]

Specifies the array of packet data. The data is an array of Int32 values which, taken in order, form the array of points (x0, y0), (x1, y1), which is passed into the method within a Variant.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param PacketDescription [in]

Is a reserved parameter that is currently not implemented.

### -param Stroke [out, retval]

When this method returns, contains a pointer to the newly-created stroke.

## -returns

This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid VARIANT type (only VT_ARRAY | VT_I4 supported).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to create the new stroke.

</td>
</tr>
</table>

## -remarks

The minimum and maximum values of any point in the points array are LONG_MIN and LONG_MAX, respectively. However, these points define an ink space rectangle whose maximum width or height cannot exceed LONG_MAX. Because of this, the difference between the minimum and maximum x-coordinates, or the minimum and maximum y-coordinates, cannot exceed LONG_MAX.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes">CreateStrokes Method</a>



<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>
