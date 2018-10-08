---
UID: NN:shdeprecated.ITrackShellMenu
title: ITrackShellMenu
author: windows-sdk-content
description: Exposes methods that extend the IShellMenu interface by providing the ability to coordinate toolbar buttons with a menu as well as display a pop-up menu.
old-location: shell\ITrackShellMenu.htm
tech.root: shell
ms.assetid: 187796db-2932-482e-833a-b4674f009b71
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ITrackShellMenu, ITrackShellMenu interface [Windows Shell], ITrackShellMenu interface [Windows Shell],described, _shell_ITrackShellMenu, shdeprecated/ITrackShellMenu, shell.ITrackShellMenu
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shdeprecated.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - ITrackShellMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITrackShellMenu interface


## -description


Exposes methods that extend the <a href="https://msdn.microsoft.com/46793ae9-936e-4a58-bc34-84396151b4a3">IShellMenu</a> interface by providing the ability to coordinate toolbar buttons with a menu as well as display a pop-up menu.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITrackShellMenu</b> interface inherits from <a href="https://msdn.microsoft.com/46793ae9-936e-4a58-bc34-84396151b4a3">IShellMenu</a>. <b>ITrackShellMenu</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITrackShellMenu</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8098143-6f36-496c-81af-f06fb83c9920">Popup</a>
</td>
<td align="left" width="63%">
Displays a modal pop-up menu at a specific location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8b73bdb-95dd-4ca7-8dc9-3318faf37338">SetObscured</a>
</td>
<td align="left" width="63%">
Coordinates obscured items on a toolbar with items in a menu.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/46793ae9-936e-4a58-bc34-84396151b4a3">IShellMenu</a> interface, from which it inherits.

This interface is implemented by the track Shell menu object. You can obtain that object by calling <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> with a class identifier (CLSID) of <code>CLSID_TrackShellMenu</code>. You can obtain interface pointers using standard Component Object Model (COM) procedures. The value of CLSID_TrackShellMenu is {8278F931-2A3E-11d2-838F-00C04FD918D0}.



