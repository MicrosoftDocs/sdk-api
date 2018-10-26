---
UID: NN:rdpappcontainerclient.IRemoteDesktopClientTouchPointer
title: IRemoteDesktopClientTouchPointer
author: windows-sdk-content
description: Provides the properties needed to control the touch pointer feature of the Remote Desktop Protocol (RDP) app container client control.
old-location: termserv\iremotedesktopclienttouchpointer.htm
tech.root: termserv
ms.assetid: 98c47e41-ecda-45cb-94e9-de51edc7af08
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IRemoteDesktopClientTouchPointer, IRemoteDesktopClientTouchPointer interface [Remote Desktop Services], IRemoteDesktopClientTouchPointer interface [Remote Desktop Services],described, rdpappcontainerclient/IRemoteDesktopClientTouchPointer, termserv.iremotedesktopclienttouchpointer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsTscAx.dll
api_name:
 - IRemoteDesktopClientTouchPointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRemoteDesktopClientTouchPointer interface


## -description



Provides the properties needed to control the touch pointer feature of the Remote Desktop Protocol (RDP) app container client control.



The touch pointer feature allows the Remote Desktop Protocol (RDP) app container client control to translate touch screen actions on the 
    client into equivalent mouse actions in the remote session. This feature is useful when the remote session is 
    running an operating system or application that is not optimized for touch screen. When the 
    <a href="https://msdn.microsoft.com/f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3">Enabled</a> property is set, the 
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




<a href="https://msdn.microsoft.com/EAF75483-90A4-4BB1-82A5-EFBB2219A55B">Remote Desktop ActiveX control reference</a>
 

 

