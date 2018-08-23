---
UID: NN:ocidl.IPointerInactive
title: IPointerInactive
author: windows-sdk-content
description: Enables an object to remain inactive most of the time, yet still participate in interaction with the mouse, including drag and drop.
old-location: com\ipointerinactive.htm
old-project: com
ms.assetid: dc08d512-6994-419a-a460-6274ce74e40f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPointerInactive, IPointerInactive interface [COM], IPointerInactive interface [COM],described, _ctrl_ipointerinactive, com.ipointerinactive, ocidl/IPointerInactive
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ocidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPointerInactive
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPointerInactive interface


## -description


Enables an object to remain inactive most of the time, yet still participate in interaction with the mouse, including drag and drop.

Objects can be active (in-place or UI active) or they can be inactive (loaded or running). An active object creates a window and can receive Windows mouse and keyboard messages. An inactive object can render itself and provide a representation of its data in a given format. While they provide more functionality, active objects also consume more resources than inactive objects. Typically, they are larger and slower than inactive objects. Thus, keeping an object inactive can provide performance improvements.

However, an object, such as a control, needs to be able to control the mouse pointer, fire mouse events, and act as a drop target so it can participate in the user interface of its container application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPointerInactive</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IPointerInactive</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPointerInactive</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbdea7e1-620f-4b2b-8ac9-77061b8cfc1a">GetActivationPolicy</a>
</td>
<td align="left" width="63%">
Retrieves the current activation policy for the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d026c570-b51b-456f-b121-eb2be08e2cac">OnInactiveMouseMove</a>
</td>
<td align="left" width="63%">
Notifies the object that the mouse pointer has moved over it so the object can fire mouse events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2c87f5e-5c8e-487c-ad18-ea95f334e01d">OnInactiveSetCursor</a>
</td>
<td align="left" width="63%">
Sets the mouse pointer for an inactive object.

</td>
</tr>
</table> 

