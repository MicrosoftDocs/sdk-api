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

# IRealTimeStylus2 interface


## -description



Extends the <a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRealTimeStylus2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRealTimeStylus2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRealTimeStylus2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b23d0a41-a5c4-40bc-a5d8-f8273119c92e">get_FlicksEnabled</a>
</td>
<td align="left" width="63%">
Enables detection of flick gestures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50bc70aa-da25-4420-87c3-ffeb9950dd34">put_FlicksEnabled</a>
</td>
<td align="left" width="63%">
Disables detection of flick gestures.

</td>
</tr>
</table> 


## -remarks



This interface only exists in the Windows Vista <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus</a>. Flick notification is recevied via a <a href="https://msdn.microsoft.com/7cdba29e-0599-45f7-8853-3e8fa29897e8">IStylusPlugin::SystemEvent Method</a> plugin notification with event id equal to <b>ISG_Flick</b>. To obtain flick data look at the <b>SYSTEM_EVENT_DATA</b> struct: <i>xPos</i>/<i>yPos</i> contains the flick start location in Tablet coordinates, <i>wKey</i> contains the direction (a value where 90 is down, 180 is left, 270 is up), and <i>dwButtonState</i> contains the same data obtained from the <i>wParam</i> for the <a href="https://msdn.microsoft.com/9433aadf-3440-4249-8f2c-3e22ebc949fb">WM_TABLET_FLICK Message</a>.




## -see-also




<a href="https://msdn.microsoft.com/5559b3a0-739b-4dd5-acf4-a44811c7cf37">Flicks API Reference</a>



<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>
 

 

