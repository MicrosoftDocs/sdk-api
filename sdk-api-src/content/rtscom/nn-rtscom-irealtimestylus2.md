---
UID: NN:rtscom.IRealTimeStylus2
title: IRealTimeStylus2 (rtscom.h)
description: Extends the IRealTimeStylus interface.
old-location: tablet\irealtimestylus2.htm
tech.root: tablet
ms.assetid: d4b55c1d-f8cc-4aed-86a3-b5935d127c2d
ms.date: 12/05/2018
ms.keywords: IRealTimeStylus2, IRealTimeStylus2 interface [Tablet PC], IRealTimeStylus2 interface [Tablet PC],described, d4b55c1d-f8cc-4aed-86a3-b5935d127c2d, rtscom/IRealTimeStylus2, tablet.irealtimestylus2
f1_keywords:
- rtscom/IRealTimeStylus2
dev_langs:
- c++
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- RTSCom.dll
api_name:
- IRealTimeStylus2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRealTimeStylus2 interface


## -description



Extends the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRealTimeStylus2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRealTimeStylus2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus2-get_flicksenabled">get_FlicksEnabled</a>
</td>
<td align="left" width="63%">
Enables detection of flick gestures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus2-put_flicksenabled">put_FlicksEnabled</a>
</td>
<td align="left" width="63%">
Disables detection of flick gestures.

</td>
</tr>
</table> 


## -remarks



This interface only exists in the Windows Vista <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus</a>. Flick notification is recevied via a <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-systemevent">IStylusPlugin::SystemEvent Method</a> plugin notification with event id equal to <b>ISG_Flick</b>. To obtain flick data look at the <b>SYSTEM_EVENT_DATA</b> struct: <i>xPos</i>/<i>yPos</i> contains the flick start location in Tablet coordinates, <i>wKey</i> contains the direction (a value where 90 is down, 180 is left, 270 is up), and <i>dwButtonState</i> contains the same data obtained from the <i>wParam</i> for the <a href="https://docs.microsoft.com/windows/desktop/tablet/wm-tablet-flick-message">WM_TABLET_FLICK Message</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/flicks-api-reference">Flicks API Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>
 

 

