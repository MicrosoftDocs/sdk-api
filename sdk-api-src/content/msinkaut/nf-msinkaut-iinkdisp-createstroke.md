---
UID: NF:msinkaut.IInkDisp.CreateStroke
title: IInkDisp::CreateStroke
author: windows-sdk-content
description: Creates an IInkStrokeDisp object from an array of packet data input values.
old-location: tablet\inkdisp_createstroke.htm
tech.root: tablet
ms.assetid: 116c5746-61ad-4a47-a5e3-4675af87b0f1
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 116c5746-61ad-4a47-a5e3-4675af87b0f1, CreateStroke, CreateStroke method [Tablet PC], CreateStroke method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],CreateStroke method, IInkDisp.CreateStroke, IInkDisp::CreateStroke, msinkaut/IInkDisp::CreateStroke, tablet.inkdisp_createstroke
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDisp::CreateStroke


## -description



Creates an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object from an array of packet data input values.




## -parameters




### -param PacketData [in]

Specifies the array of packet data. The data is an array of Int32 values which, taken in order, form the array of points (x0, y0), (x1, y1), which is passed into the method within a Variant.

For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


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




<a href="https://msdn.microsoft.com/21e68151-38c9-414f-840c-c2687a05aea4">CreateStrokes Method</a>



<a href="https://msdn.microsoft.com/85B683AA-D859-4717-8C61-C0EB4BBA5F61">IInkDisp</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>
 

 

