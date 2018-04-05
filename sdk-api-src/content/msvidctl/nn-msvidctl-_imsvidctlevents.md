---
UID: NN:msvidctl._IMSVidCtlEvents
title: "_IMSVidCtlEvents"
author: windows-driver-content
description: This topic applies to Windows XP or later.
old-location: mstv\_imsvidctlevents.htm
old-project: mstv
ms.assetid: c28ccbf6-17eb-4cc3-bbae-3bd7eb92bb01
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "_IMSVidCtlEvents, _IMSVidCtlEvents interface [Microsoft TV Technologies], _IMSVidCtlEvents interface [Microsoft TV Technologies], described, _IMSVidCtlEventsInterface, mstv._imsvidctlevents, msvidctl/_IMSVidCtlEvents"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msvidctl.h
api_name:
-	_IMSVidCtlEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _IMSVidCtlEvents interface


## -description



This topic applies to Windows XP or later.
        

The <b>_IMSVidCtlEvents</b> interface is used to receive events from the Video Control.

This interface is an outgoing connection-point interface. To receive events from the Video Control, implement this interface in your application. Then call the <b>IConnectionPoint::Advise</b> method on the Video Control to establish a connection.

<b>_IMSVidCtlEvents</b> is a dispinterface, invoked through <b>IDispatch</b>. The dispatch identifier is DIID__IMSVidCtlEvents. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">_IMSVidCtlEvents</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>_IMSVidCtlEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>_IMSVidCtlEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ef316dd-99e3-474e-bb87-8ba7983fccd2">Click</a>
</td>
<td align="left" width="63%">
Called when a user clicks anywhere on the Video Control's rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac6b63b9-041f-4e8a-ab88-aee8333291cd">DblClick</a>
</td>
<td align="left" width="63%">
Called when a user double-clicks on the Video Control's rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a1c0cca-b708-4f51-ada0-49a356759ce7">Error</a>
</td>
<td align="left" width="63%">
Called when an error occurs in the control or the underlying filter graph. Currently no errors are defined for this event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e377272-54ac-43d9-9741-9ccd0f6843c2">KeyDown</a>
</td>
<td align="left" width="63%">
Called when the user presses a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0315c20-c403-44a8-b2aa-8a8b8c124b28">KeyPress</a>
</td>
<td align="left" width="63%">
Called when the user presses and releases a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f4245ab-44eb-42e0-a5da-ed55521e1b28">KeyUp</a>
</td>
<td align="left" width="63%">
Called when the user releases a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5767d770-4b8f-44f2-8b2d-6d55ec6cd854">MouseDown</a>
</td>
<td align="left" width="63%">
Called when the user presses the left mouse key down while the mouse pointer is over the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57549fae-b056-4180-b391-af87274443c6">MouseMove</a>
</td>
<td align="left" width="63%">
Called when the user moves the mouse pointer over the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/717d3f08-1589-4f44-bdf8-02e4800d2298">MouseUp</a>
</td>
<td align="left" width="63%">
Called when the user releases the left mouse button while the mouse pointer is over the Video Control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16dca4ab-be3d-493a-892b-8d90a0baf109">StateChange</a>
</td>
<td align="left" width="63%">
Called when the state of the Video Control changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

