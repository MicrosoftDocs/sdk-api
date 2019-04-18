---
UID: NN:wmp.IWMPEvents
title: IWMPEvents (wmp.h)
author: windows-sdk-content
description: The IWMPEvents interface provides events that originate from the Windows Media Player control. An embedding program can respond to these events. The events exposed by IWMPEvents are also exposed by the _WMPOCXEvents interface.
old-location: wmp\iwmpevents_interface.htm
tech.root: WMP
ms.assetid: 396545d5-8844-4dd2-9ed5-e4ed77f352ac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPEvents, IWMPEvents interface [Windows Media Player], IWMPEvents interface [Windows Media Player],described, IWMPEventsInterface, wmp.iwmpevents_interface, wmp/IWMPEvents
ms.topic: interface
req.header: wmp.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEvents interface


## -description



The <b>IWMPEvents</b> interface provides events that originate from the Windows Media Player control. An embedding program can respond to these events. The events exposed by <b>IWMPEvents</b> are also exposed by the <b>_WMPOCXEvents</b> interface.



In addition to the methods inherited from <b>IUnknown</b>, the <b>IWMPEvents</b> interface exposes the following methods.
<table>
<tr>
<th>Method
          </th>
<th>Description
          </th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563311(v=VS.85).aspx">AudioLanguageChange</a>
</td>
<td>Occurs when the current audio language changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563312(v=VS.85).aspx">Buffering</a>
</td>
<td>Occurs when the Windows Media Player control begins or ends buffering.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563313(v=VS.85).aspx">CdromMediaChange</a>
</td>
<td>Occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563314(v=VS.85).aspx">Click</a>
</td>
<td>Occurs when the user clicks a mouse button.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563315(v=VS.85).aspx">CurrentItemChange</a>
</td>
<td>Occurs when the <b>currentItem</b> property of the <b>IWMPControls</b> interface changes value.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563316(v=VS.85).aspx">CurrentMediaItemAvailable</a>
</td>
<td>Occurs when the current media item becomes available.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563317(v=VS.85).aspx">CurrentPlaylistChange</a>
</td>
<td>Occurs when something changes within the current playlist.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563318(v=VS.85).aspx">CurrentPlaylistItemAvailable</a>
</td>
<td>Occurs when the current playlist item becomes available.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563319(v=VS.85).aspx">Disconnect</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563320(v=VS.85).aspx">DomainChange</a>
</td>
<td>Occurs when the DVD domain changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563321(v=VS.85).aspx">DoubleClick</a>
</td>
<td>Occurs when the user double-clicks a mouse button.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563322(v=VS.85).aspx">DurationUnitChange</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563323(v=VS.85).aspx">EndOfStream</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563324(v=VS.85).aspx">Error</a>
</td>
<td>Occurs when the Windows Media Player control has an error condition.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563325(v=VS.85).aspx">KeyDown</a>
</td>
<td>Occurs when a key is pressed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563326(v=VS.85).aspx">KeyPress</a>
</td>
<td>Occurs when a key is pressed and then released.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563327(v=VS.85).aspx">KeyUp</a>
</td>
<td>Occurs when a key is released.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563328(v=VS.85).aspx">MarkerHit</a>
</td>
<td>Occurs when a marker is reached.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563329(v=VS.85).aspx">MediaChange</a>
</td>
<td>Occurs when a media item changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563340(v=VS.85).aspx">MediaCollectionAttributeStringAdded</a>
</td>
<td>Occurs when an attribute is added to the library.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563341(v=VS.85).aspx">MediaCollectionAttributeStringChanged</a>
</td>
<td>Occurs when an attribute in the library is changed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563342(v=VS.85).aspx">MediaCollectionAttributeStringRemoved</a>
</td>
<td>Occurs when an attribute is removed from the library.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563343(v=VS.85).aspx">MediaCollectionChange</a>
</td>
<td>Occurs when the media collection changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563344(v=VS.85).aspx">MediaError</a>
</td>
<td>Occurs when the <b>Media</b> object has an error condition.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563345(v=VS.85).aspx">ModeChange</a>
</td>
<td>Occurs when a mode of Windows Media Player is changed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563346(v=VS.85).aspx">MouseDown</a>
</td>
<td>Occurs when a mouse button is pressed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563347(v=VS.85).aspx">MouseMove</a>
</td>
<td>Occurs when the mouse pointer is moved.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563348(v=VS.85).aspx">MouseUp</a>
</td>
<td>Occurs when a mouse button is released.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563349(v=VS.85).aspx">NewStream</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563350(v=VS.85).aspx">OpenPlaylistSwitch</a>
</td>
<td>Occurs when a title on a DVD begins playing.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563351(v=VS.85).aspx">OpenStateChange</a>
</td>
<td>Occurs when the Windows Media Player control changes state.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563352(v=VS.85).aspx">PlayerDockedStateChange</a>
</td>
<td>Occurs when a remoted Windows Media Player control docks or undocks.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563353(v=VS.85).aspx">PlayerReconnect</a>
</td>
<td>Occurs when a remoted Windows Media Player control reconnects to the Player.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563354(v=VS.85).aspx">PlaylistChange</a>
</td>
<td>Occurs when a playlist changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563355(v=VS.85).aspx">PlaylistCollectionChange</a>
</td>
<td>Occurs when something changes in the playlist collection.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563356(v=VS.85).aspx">PlaylistCollectionPlaylistAdded</a>
</td>
<td>Occurs when a playlist is added to the playlist collection.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563357(v=VS.85).aspx">PlaylistCollectionPlaylistRemoved</a>
</td>
<td>Occurs when a playlist is removed from the playlist collection.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563358(v=VS.85).aspx">PlaylistCollectionPlaylistSetAsDeleted</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563359(v=VS.85).aspx">PlayStateChange</a>
</td>
<td>Occurs when the play state of the Windows Media Player control changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563360(v=VS.85).aspx">PositionChange</a>
</td>
<td>Occurs when the current position of the media has been changed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563361(v=VS.85).aspx">ScriptCommand</a>
</td>
<td>Occurs when a synchronized command or URL is received.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563362(v=VS.85).aspx">StatusChange</a>
</td>
<td>Occurs when the <b>status</b> property changes value.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563363(v=VS.85).aspx">SwitchedToControl</a>
</td>
<td>Occurs when a remoted Windows Media Player control switches to the docked state.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563364(v=VS.85).aspx">SwitchedToPlayerApplication</a>
</td>
<td>Occurs when a remoted Windows Media Player control switches to the full mode of the Player.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563365(v=VS.85).aspx">Warning</a>
</td>
<td>Reserved for future use.</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563289(v=VS.85).aspx">IWMPEvents2 Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

