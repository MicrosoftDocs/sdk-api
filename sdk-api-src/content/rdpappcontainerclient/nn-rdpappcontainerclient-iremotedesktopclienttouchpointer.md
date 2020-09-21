---
UID: NN:rdpappcontainerclient.IRemoteDesktopClientTouchPointer
title: IRemoteDesktopClientTouchPointer (rdpappcontainerclient.h)
description: Provides the properties needed to control the touch pointer feature of the Remote Desktop Protocol (RDP) app container client control.
helpviewer_keywords: ["IRemoteDesktopClientTouchPointer","IRemoteDesktopClientTouchPointer interface [Remote Desktop Services]","IRemoteDesktopClientTouchPointer interface [Remote Desktop Services]","described","rdpappcontainerclient/IRemoteDesktopClientTouchPointer","termserv.iremotedesktopclienttouchpointer"]
old-location: termserv\iremotedesktopclienttouchpointer.htm
tech.root: TermServ
ms.assetid: 98c47e41-ecda-45cb-94e9-de51edc7af08
ms.date: 12/05/2018
ms.keywords: IRemoteDesktopClientTouchPointer, IRemoteDesktopClientTouchPointer interface [Remote Desktop Services], IRemoteDesktopClientTouchPointer interface [Remote Desktop Services],described, rdpappcontainerclient/IRemoteDesktopClientTouchPointer, termserv.iremotedesktopclienttouchpointer
req.header: rdpappcontainerclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsTscAx.dll
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRemoteDesktopClientTouchPointer
 - rdpappcontainerclient/IRemoteDesktopClientTouchPointer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsTscAx.dll
api_name:
 - IRemoteDesktopClientTouchPointer
---

# IRemoteDesktopClientTouchPointer interface


## -description

Provides the properties needed to control the touch pointer feature of the Remote Desktop Protocol (RDP) app container client control.



The touch pointer feature allows the Remote Desktop Protocol (RDP) app container client control to translate touch screen actions on the 
    client into equivalent mouse actions in the remote session. This feature is useful when the remote session is 
    running an operating system or application that is not optimized for touch screen. When the 
    <a href="/windows/desktop/TermServ/iremotedesktopclienttouchpointer-enabled">Enabled</a> property is set, the 
    RDP app container client control will interpret certain touch gestures and translate them into mouse events in the 
    remote session. These translations make it easier for the user to simulate certain mouse actions that do not 
    readily translate to touch screen gestures, such as right-click and drag.

The following is a list of client touch-screen gestures and their corresponding remote session mouse events.
<table>
<tr>
<th>Client touch-screen gesture</th>
<th>Remote session mouse event</th>
</tr>
<tr>
<td>
Tap

</td>
<td>
Left button click

</td>
</tr>
<tr>
<td>
Drag

</td>
<td>
Cursor move

</td>
</tr>
<tr>
<td>
Press and hold with one finger, then tap with another finger to the right of the first finger

</td>
<td>
Right button click

</td>
</tr>
<tr>
<td>
Press and hold with one finger, then press and hold with another finger to the left of the first finger

</td>
<td>
Left button click and hold

</td>
</tr>
<tr>
<td>
Press and hold with one finger, then press and hold with another finger to the right of the first finger

</td>
<td>
Right button click and hold

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/TermServ/remote-desktop-activex-control-reference">Remote Desktop ActiveX control reference</a>