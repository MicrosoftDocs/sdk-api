---
UID: NF:msinkaut.IInkOverlay.SetEventInterest
title: IInkOverlay::SetEventInterest
author: windows-sdk-content
description: Sets a value that indicates whether an object or control has interest in a specified event.
old-location: tablet\inkoverlay_seteventinterest.htm
old-project: tablet
ms.assetid: 046eb6be-ac7c-4cf8-82e8-f58d9d826682
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IInkOverlay interface [Tablet PC],SetEventInterest method, IInkOverlay.SetEventInterest, IInkOverlay::SetEventInterest, SetEventInterest, SetEventInterest method [Tablet PC], SetEventInterest method [Tablet PC],IInkOverlay interface, df25efbb-5229-4211-948f-3a213154a967, msinkaut/IInkOverlay::SetEventInterest, tablet.inkoverlay_seteventinterest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkOverlay::SetEventInterest


## -description



Sets a value that indicates whether an object or control has interest in a specified event.




## -parameters




### -param EventId [in]

The event to be listened for. Possible values for <i>EventID</i> appear in the <a href="https://msdn.microsoft.com/db575790-345b-48da-b509-927eb2f47987">InkCollectorEventInterest</a> enumeration type.


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



All ink collector  events can be toggled by using this method. Most of these events are turned off by default for performance reasons. The only events that are on by default are <a href="https://msdn.microsoft.com/eaa89dfe-6141-4205-845b-634321130e26">Stroke</a>, <a href="https://msdn.microsoft.com/d05b240c-ba64-4008-b25d-e06c052eb5b0">CursorInRange</a>, and <a href="https://msdn.microsoft.com/a3a570ed-570b-4579-b120-ed5457630bc2">CursorOutOfRange</a>.

Use the <a href="https://msdn.microsoft.com/2682e7ba-dabd-497e-aea4-6d3f837f4f10">NewPackets</a>, <a href="https://msdn.microsoft.com/e8eacdec-0381-435f-b453-24dca1c507c9">NewInAirPackets</a> and <a href="https://msdn.microsoft.com/bf914849-ef33-4746-b2e1-c768cd1d87aa">CursorDown</a> events carefully, in particular because they may have an adverse effect on ink performance if too much code is executed in the event handlers.




## -see-also




<a href="https://msdn.microsoft.com/bf914849-ef33-4746-b2e1-c768cd1d87aa">CursorDown Event</a>



<a href="https://msdn.microsoft.com/d05b240c-ba64-4008-b25d-e06c052eb5b0">CursorInRange Event</a>



<a href="https://msdn.microsoft.com/532a798e-b434-4730-8c20-7ec60255f170">GetEventInterest Method</a>



<a href="https://msdn.microsoft.com/ACE11946-113B-42EE-A3F1-0036B1DF8141">IInkOverlay</a>



<a href="https://msdn.microsoft.com/db575790-345b-48da-b509-927eb2f47987">InkCollectorEventInterest Enumeration</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/2682e7ba-dabd-497e-aea4-6d3f837f4f10">NewPackets Event</a>



<a href="https://msdn.microsoft.com/eaa89dfe-6141-4205-845b-634321130e26">Stroke Event</a>
 

 

