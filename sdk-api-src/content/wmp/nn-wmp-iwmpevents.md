---
UID: NN:wmp.IWMPEvents
title: IWMPEvents (wmp.h)
description: The IWMPEvents interface provides events that originate from the Windows Media Player control. An embedding program can respond to these events. The events exposed by IWMPEvents are also exposed by the _WMPOCXEvents interface.
helpviewer_keywords: ["IWMPEvents","IWMPEvents interface [Windows Media Player]","IWMPEvents interface [Windows Media Player]","described","IWMPEventsInterface","wmp.iwmpevents_interface","wmp/IWMPEvents"]
old-location: wmp\iwmpevents_interface.htm
tech.root: WMP
ms.assetid: 396545d5-8844-4dd2-9ed5-e4ed77f352ac
ms.date: 4/26/2023
ms.keywords: IWMPEvents, IWMPEvents interface [Windows Media Player], IWMPEvents interface [Windows Media Player],described, IWMPEventsInterface, wmp.iwmpevents_interface, wmp/IWMPEvents
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents
 - wmp/IWMPEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPEvents
---

# IWMPEvents interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-audiolanguagechange">AudioLanguageChange</a>
</td>
<td>Occurs when the current audio language changes.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-buffering">Buffering</a>
</td>
<td>Occurs when the Windows Media Player control begins or ends buffering.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-cdrommediachange">CdromMediaChange</a>
</td>
<td>Occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-click">Click</a>
</td>
<td>Occurs when the user clicks a mouse button.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-currentitemchange">CurrentItemChange</a>
</td>
<td>Occurs when the <b>currentItem</b> property of the <b>IWMPControls</b> interface changes value.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-currentmediaitemavailable">CurrentMediaItemAvailable</a>
</td>
<td>Occurs when the current media item becomes available.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-currentplaylistchange">CurrentPlaylistChange</a>
</td>
<td>Occurs when something changes within the current playlist.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-currentplaylistitemavailable">CurrentPlaylistItemAvailable</a>
</td>
<td>Occurs when the current playlist item becomes available.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-disconnect">Disconnect</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-domainchange">DomainChange</a>
</td>
<td>Occurs when the DVD domain changes.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-doubleclick">DoubleClick</a>
</td>
<td>Occurs when the user double-clicks a mouse button.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-durationunitchange">DurationUnitChange</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-endofstream">EndOfStream</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-error">Error</a>
</td>
<td>Occurs when the Windows Media Player control has an error condition.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-keydown">KeyDown</a>
</td>
<td>Occurs when a key is pressed.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-keypress">KeyPress</a>
</td>
<td>Occurs when a key is pressed and then released.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-keyup">KeyUp</a>
</td>
<td>Occurs when a key is released.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-markerhit">MarkerHit</a>
</td>
<td>Occurs when a marker is reached.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange">MediaChange</a>
</td>
<td>Occurs when a media item changes.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediacollectionattributestringadded">MediaCollectionAttributeStringAdded</a>
</td>
<td>Occurs when an attribute is added to the library.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediacollectionattributestringchanged">MediaCollectionAttributeStringChanged</a>
</td>
<td>Occurs when an attribute in the library is changed.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediacollectionattributestringremoved">MediaCollectionAttributeStringRemoved</a>
</td>
<td>Occurs when an attribute is removed from the library.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediacollectionchange">MediaCollectionChange</a>
</td>
<td>Occurs when the media collection changes.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediaerror">MediaError</a>
</td>
<td>Occurs when the <b>Media</b> object has an error condition.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-modechange">ModeChange</a>
</td>
<td>Occurs when a mode of Windows Media Player is changed.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-mousedown">MouseDown</a>
</td>
<td>Occurs when a mouse button is pressed.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-mousemove">MouseMove</a>
</td>
<td>Occurs when the mouse pointer is moved.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-mouseup">MouseUp</a>
</td>
<td>Occurs when a mouse button is released.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-newstream">NewStream</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-openplaylistswitch">OpenPlaylistSwitch</a>
</td>
<td>Occurs when a title on a DVD begins playing.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-openstatechange">OpenStateChange</a>
</td>
<td>Occurs when the Windows Media Player control changes state.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange">PlayerDockedStateChange</a>
</td>
<td>Occurs when a remoted Windows Media Player control docks or undocks.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect">PlayerReconnect</a>
</td>
<td>Occurs when a remoted Windows Media Player control reconnects to the Player.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-playlistchange">PlaylistChange</a>
</td>
<td>Occurs when a playlist changes.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-playlistcollectionchange">PlaylistCollectionChange</a>
</td>
<td>Occurs when something changes in the playlist collection.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-playlistcollectionplaylistadded">PlaylistCollectionPlaylistAdded</a>
</td>
<td>Occurs when a playlist is added to the playlist collection.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-playlistcollectionplaylistremoved">PlaylistCollectionPlaylistRemoved</a>
</td>
<td>Occurs when a playlist is removed from the playlist collection.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-playlistcollectionplaylistsetasdeleted">PlaylistCollectionPlaylistSetAsDeleted</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-playstatechange">PlayStateChange</a>
</td>
<td>Occurs when the play state of the Windows Media Player control changes.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-positionchange">PositionChange</a>
</td>
<td>Occurs when the current position of the media has been changed.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-scriptcommand">ScriptCommand</a>
</td>
<td>Occurs when a synchronized command or URL is received.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-statuschange">StatusChange</a>
</td>
<td>Occurs when the <b>status</b> property changes value.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol">SwitchedToControl</a>
</td>
<td>Occurs when a remoted Windows Media Player control switches to the docked state.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication">SwitchedToPlayerApplication</a>
</td>
<td>Occurs when a remoted Windows Media Player control switches to the full mode of the Player.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-warning">Warning</a>
</td>
<td>Reserved for future use.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2 Interface</a>



<a href="/windows/desktop/WMP/interfaces">Interfaces</a>