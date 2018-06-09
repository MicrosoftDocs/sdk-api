---
UID: NF:msinkaut.IInkPicture.SetEventInterest
title: IInkPicture::SetEventInterest
author: windows-sdk-content
description: Modifies a value that indicates whether an object or control has interest in a specified event.
old-location: tablet\inkpicture_seteventinterest.htm
old-project: tablet
ms.assetid: 4baaf348-dec7-4b81-8415-b9f4ace14f5d
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IInkPicture, IInkPicture interface [Tablet PC],SetEventInterest method, IInkPicture.SetEventInterest, IInkPicture::SetEventInterest, SetEventInterest, SetEventInterest method [Tablet PC], SetEventInterest method [Tablet PC],IInkPicture interface, df25efbb-5229-4211-948f-3a213154a967, msinkaut/IInkPicture::SetEventInterest, tablet.inkpicture_seteventinterest
ms.prod: windows
ms.technology: windows-sdk
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
 - IInkPicture.SetEventInterest
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkPicture::SetEventInterest


## -description



Modifies a value that indicates whether an object or control has interest in a specified event.




## -parameters




### -param EventId [in]

The event to be listened for. Possible values for <i>eventID</i> appear in the <a href="https://msdn.microsoft.com/db575790-345b-48da-b509-927eb2f47987">InkCollectorEventInterest</a> enumeration type.


### -param Listen [in]

<b>VARIANT_TRUE</b> to indicate the event is being used; <b>VARIANT_FALSE</b> to indicate the event is being ignored.


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



All ink collector  events can be toggled by using this method. Most of these events are turned off by default for performance reasons. The only events that are on by default are <a href="https://msdn.microsoft.com/2829b65a-6120-402e-91e3-5587d1f456f9">Stroke</a>, <a href="https://msdn.microsoft.com/e921e175-a2cf-45e6-bb81-dc82e384d3b1">CursorInRange</a>, and <a href="https://msdn.microsoft.com/0c71a4ad-3c09-4134-b0e7-82f29e8913ed">CursorOutOfRange</a>.

Use the <a href="https://msdn.microsoft.com/7d120198-c016-4452-b8a8-22c4ad87d526">NewPackets</a>, <a href="https://msdn.microsoft.com/30bc423d-0642-4515-9e51-a8b8b36aecad">NewInAirPackets</a> and <a href="https://msdn.microsoft.com/6d524400-1341-45da-86b2-098e34ed5a1c">CursorDown</a> events carefully, in particular because they may have an adverse effect on ink performance if too much code is executed in the event handlers.




## -see-also




<a href="https://msdn.microsoft.com/6d524400-1341-45da-86b2-098e34ed5a1c">CursorDown Event</a>



<a href="https://msdn.microsoft.com/e921e175-a2cf-45e6-bb81-dc82e384d3b1">CursorInRange Event</a>



<a href="https://msdn.microsoft.com/e025a118-acf1-4b52-ace9-85a3a5a558fa">GetEventInterest Method</a>



<a href="tablet.iinkpicture">IInkPicture</a>



<a href="https://msdn.microsoft.com/db575790-345b-48da-b509-927eb2f47987">InkCollectorEventInterest Enumeration</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>



<a href="https://msdn.microsoft.com/7d120198-c016-4452-b8a8-22c4ad87d526">NewPackets Event</a>



<a href="https://msdn.microsoft.com/2829b65a-6120-402e-91e3-5587d1f456f9">Stroke Event</a>
 

 

