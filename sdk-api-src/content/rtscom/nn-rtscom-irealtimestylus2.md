---
UID: NN:rtscom.IRealTimeStylus2
title: IRealTimeStylus2
author: windows-sdk-content
description: Extends the IRealTimeStylus interface.
old-location: tablet\irealtimestylus2.htm
old-project: tablet
ms.assetid: d4b55c1d-f8cc-4aed-86a3-b5935d127c2d
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IRealTimeStylus2, IRealTimeStylus2 interface [Tablet PC], IRealTimeStylus2 interface [Tablet PC],described, d4b55c1d-f8cc-4aed-86a3-b5935d127c2d, rtscom/IRealTimeStylus2, tablet.irealtimestylus2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus2
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
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
 

 

