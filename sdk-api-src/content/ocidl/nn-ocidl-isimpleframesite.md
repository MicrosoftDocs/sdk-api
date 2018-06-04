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

# ISimpleFrameSite interface


## -description


Provides simple frame controls that act as simple containers for other nested controls. Some controls merely contain other controls. In such cases, the simple control container, called a simple frame, need not implement all container requirements. It can delegate most of the interface calls from its contained controls to the outer container that manages the simple frame. To support what are called simple frame controls, a container implements this interface as well as other site interfaces such as <a href="https://msdn.microsoft.com/8b022f2c-d4b4-44ca-8e69-46e9aa20b3f9">IOleControlSite</a>.

An example of a simple frame control is a group box that only needs to capture a few keystrokes for its contained controls to implement the correct tab or arrow key behavior, but does not want to handle every other message. Through the two methods of this interface, the simple frame control passes messages to its control site both before and after its own processing. If that site is itself a simple frame, it can continue to pass messages up the chain.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimpleFrameSite</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ISimpleFrameSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISimpleFrameSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9725ef9-16e0-4574-9b94-826814a396be">PostMessageFilter</a>
</td>
<td align="left" width="63%">
Sends the simple frame site a message that is received by a control's own window after the control has processed the message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f308ea77-12e7-450b-8b0f-252f1d240388">PreMessageFilter</a>
</td>
<td align="left" width="63%">
Provides a site with the opportunity to process a message that is received by a control's own window before the control itself does any processing.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ef85dce6-b680-4a72-9277-4cfdab27cbbc">IOleControl</a>



<a href="https://msdn.microsoft.com/8b022f2c-d4b4-44ca-8e69-46e9aa20b3f9">IOleControlSite</a>
 

 

