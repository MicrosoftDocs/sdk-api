---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

