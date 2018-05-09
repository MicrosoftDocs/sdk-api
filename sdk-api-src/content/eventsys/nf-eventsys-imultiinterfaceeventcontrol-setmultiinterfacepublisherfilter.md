---
UID: NF:eventsys.IMultiInterfaceEventControl.SetMultiInterfacePublisherFilter
title: IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter
author: windows-driver-content
description: Assigns a publisher filter to an event method at run time.
old-location: cos\imultiinterfaceeventcontrol_setmultiinterfacepublisherfilter.htm
old-project: cossdk
ms.assetid: 0eb52937-3bd8-45ab-b4ba-c0264c47c909
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IMultiInterfaceEventControl interface [COM+],SetMultiInterfacePublisherFilter method, IMultiInterfaceEventControl.SetMultiInterfacePublisherFilter, IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter, SetMultiInterfacePublisherFilter, SetMultiInterfacePublisherFilter method [COM+], SetMultiInterfacePublisherFilter method [COM+],IMultiInterfaceEventControl interface, _cos_IMultiInterfaceEventControl_SetMultiInterfacePublisherFilter, cos.imultiinterfaceeventcontrol_setmultiinterfacepublisherfilter, eventsys/IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EventSys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EventSys.h
api_name:
-	IMultiInterfaceEventControl.SetMultiInterfacePublisherFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMultiInterfaceEventControl::SetMultiInterfacePublisherFilter


## -description


Assigns a publisher filter to an event method at run time.

This method sets the specified publisher filter for all methods of all event interfaces for the event object.


## -parameters




### -param classFilter [in]

A pointer to the <a href="https://msdn.microsoft.com/f20f778b-fdd5-4c34-871b-d03cd1cd31cc">IMultiInterfacePublisherFilter</a> interface on the publisher filter associated with the specified method.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_INTERNALEXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An unexpected exception was raised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_INTERNALERROR</b></dt>
</dl>
</td>
<td width="60%">
An unexpected internal error was detected.

</td>
</tr>
</table>
 




## -remarks



An event publisher can install a publisher filter at run time to fire an event only to subscribers that meet the criteria specified in the filter.




## -see-also




<a href="https://msdn.microsoft.com/e603f68a-881c-468d-a3d3-738f43400e01">IMultiInterfaceEventControl</a>
 

 

