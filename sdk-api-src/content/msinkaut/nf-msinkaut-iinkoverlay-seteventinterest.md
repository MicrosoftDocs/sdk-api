---
UID: NF:msinkaut.IInkOverlay.SetEventInterest
title: IInkOverlay::SetEventInterest (msinkaut.h)
description: Sets a value that indicates whether an object or control has interest in a specified event.
helpviewer_keywords: ["IInkOverlay interface [Tablet PC]","SetEventInterest method","IInkOverlay.SetEventInterest","IInkOverlay::SetEventInterest","SetEventInterest","SetEventInterest method [Tablet PC]","SetEventInterest method [Tablet PC]","IInkOverlay interface","df25efbb-5229-4211-948f-3a213154a967","msinkaut/IInkOverlay::SetEventInterest","tablet.inkoverlay_seteventinterest"]
old-location: tablet\inkoverlay_seteventinterest.htm
tech.root: tablet
ms.assetid: 046eb6be-ac7c-4cf8-82e8-f58d9d826682
ms.date: 12/05/2018
ms.keywords: IInkOverlay interface [Tablet PC],SetEventInterest method, IInkOverlay.SetEventInterest, IInkOverlay::SetEventInterest, SetEventInterest, SetEventInterest method [Tablet PC], SetEventInterest method [Tablet PC],IInkOverlay interface, df25efbb-5229-4211-948f-3a213154a967, msinkaut/IInkOverlay::SetEventInterest, tablet.inkoverlay_seteventinterest
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
 - IInkOverlay::SetEventInterest
 - msinkaut/IInkOverlay::SetEventInterest
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
 - IInkOverlay.SetEventInterest
---

# IInkOverlay::SetEventInterest


## -description

Sets a value that indicates whether an object or control has interest in a specified event.

## -parameters

### -param EventId [in]

The event to be listened for. Possible values for <i>EventID</i> appear in the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectoreventinterest">InkCollectorEventInterest</a> enumeration type.

### -param Listen [in]

<b>VARIANT_TRUE</b> if the event is being used and <b>VARIANT_FALSE</b> if it is being ignored.

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
Invalid event interest.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred during processing.

</td>
</tr>
</table>

## -remarks

All ink collector  events can be toggled by using this method. Most of these events are turned off by default for performance reasons. The only events that are on by default are <a href="/windows/desktop/tablet/inkcollector-stroke">Stroke</a>, <a href="/windows/desktop/tablet/inkcollector-cursorinrange">CursorInRange</a>, and <a href="/windows/desktop/tablet/inkcollector-cursoroutofrange">CursorOutOfRange</a>.

Use the <a href="/windows/desktop/tablet/inkcollector-newpackets">NewPackets</a>, <a href="/windows/desktop/tablet/inkcollector-newinairpackets">NewInAirPackets</a> and <a href="/windows/desktop/tablet/inkcollector-cursordown">CursorDown</a> events carefully, in particular because they may have an adverse effect on ink performance if too much code is executed in the event handlers.

## -see-also

<a href="/windows/desktop/tablet/inkcollector-cursordown">CursorDown Event</a>



<a href="/windows/desktop/tablet/inkcollector-cursorinrange">CursorInRange Event</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest">GetEventInterest Method</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846799(v=VS.85).aspx">IInkOverlay</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectoreventinterest">InkCollectorEventInterest Enumeration</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/tablet/inkcollector-newpackets">NewPackets Event</a>



<a href="/windows/desktop/tablet/inkcollector-stroke">Stroke Event</a>