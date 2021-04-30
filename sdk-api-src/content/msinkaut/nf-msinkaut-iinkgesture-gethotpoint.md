---
UID: NF:msinkaut.IInkGesture.GetHotPoint
title: IInkGesture::GetHotPoint (msinkaut.h)
description: Gets the hot point of the gesture, in ink space coordinates.
helpviewer_keywords: ["6c047cf7-2162-4146-906b-47c4006daeeb","GetHotPoint","GetHotPoint method [Tablet PC]","GetHotPoint method [Tablet PC]","IInkGesture interface","IInkGesture interface [Tablet PC]","GetHotPoint method","IInkGesture.GetHotPoint","IInkGesture::GetHotPoint","msinkaut/IInkGesture::GetHotPoint","tablet.iinkgesture_gethotpoint"]
old-location: tablet\iinkgesture_gethotpoint.htm
tech.root: tablet
ms.assetid: 6c047cf7-2162-4146-906b-47c4006daeeb
ms.date: 12/05/2018
ms.keywords: 6c047cf7-2162-4146-906b-47c4006daeeb, GetHotPoint, GetHotPoint method [Tablet PC], GetHotPoint method [Tablet PC],IInkGesture interface, IInkGesture interface [Tablet PC],GetHotPoint method, IInkGesture.GetHotPoint, IInkGesture::GetHotPoint, msinkaut/IInkGesture::GetHotPoint, tablet.iinkgesture_gethotpoint
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
 - IInkGesture::GetHotPoint
 - msinkaut/IInkGesture::GetHotPoint
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
 - IInkGesture.GetHotPoint
---

# IInkGesture::GetHotPoint


## -description

Gets the hot point of the gesture, in ink space coordinates.

## -parameters

### -param X [in, out]

The X-value of the hot point, in ink space coordinates.

### -param Y [in, out]

The Y-value of the hot point, in ink space coordinates.

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
Error information is provided.

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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred while processing.

</td>
</tr>
</table>

## -remarks

The hot point is the one distinguishing point of a gesture. It is usually the point of the angle in a gesture or the point at which the gesture is intended to occur in relation to the content around it. If there is no discernable hot point for a known gesture, the starting point of the gesture is the hot point.

For example, the hot point of the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">Check</a> gesture is the point of the angle, and the hot point of the <b>Curlicue</b> gesture is the start of the stroke that is the gesture.

For more information about how a hot point is used, see <a href="/windows/desktop/tablet/using-gestures">Using Gestures</a>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture">IInkGesture Interface</a>



<a href="/windows/desktop/tablet/using-gestures">Using Gestures</a>