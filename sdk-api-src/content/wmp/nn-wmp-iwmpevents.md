---
UID: NN:wmp.IWMPEvents
title: IWMPEvents
author: windows-sdk-content
description: The IWMPEvents interface provides events that originate from the Windows Media Player control. An embedding program can respond to these events. The events exposed by IWMPEvents are also exposed by the _WMPOCXEvents interface.
old-location: wmp\iwmpevents_interface.htm
old-project: WMP
ms.assetid: 396545d5-8844-4dd2-9ed5-e4ed77f352ac
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPEvents, IWMPEvents interface [Windows Media Player], IWMPEvents interface [Windows Media Player],described, IWMPEventsInterface, wmp.iwmpevents_interface, wmp/IWMPEvents
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.h
api_name:
-	IWMPEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents interface


## -description



The <b>IWMPEvents</b> interface provides events that originate from the Windows Media Player control. An embedding program can respond to these events. The events exposed by <b>IWMPEvents</b> are also exposed by the <b>_WMPOCXEvents</b> interface.



In addition to the methods inherited from <b>IUnknown</b>, the <b>IWMPEvents</b> interface exposes the following methods.
<table>
<tr>
<th>
            Method
          </th>
<th>
            Description
          </th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c1dbe76f-5cc0-4c12-98bb-2586ee8773d5">AudioLanguageChange</a>
</td>
<td>Occurs when the current audio language changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/mt604174">Buffering</a>
</td>
<td>Occurs when the Windows Media Player control begins or ends buffering.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/019ab066-ae2b-4517-bc1c-d96bb6e8e15e">CdromMediaChange</a>
</td>
<td>Occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6535012d-61d5-4200-8de9-786c633cf079">Click</a>
</td>
<td>Occurs when the user clicks a mouse button.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3669fe6e-233e-4214-9f84-763a06835f48">CurrentItemChange</a>
</td>
<td>Occurs when the <b>currentItem</b> property of the <b>IWMPControls</b> interface changes value.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8e6e92b7-1916-4628-915b-e9ee0d52fe75">CurrentMediaItemAvailable</a>
</td>
<td>Occurs when the current media item becomes available.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b8020b8a-4f2e-4039-862e-9c0f371645fa">CurrentPlaylistChange</a>
</td>
<td>Occurs when something changes within the current playlist.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/77209df0-3b3d-4fc8-b560-a2c02138e746">CurrentPlaylistItemAvailable</a>
</td>
<td>Occurs when the current playlist item becomes available.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6fa2f206-1eea-4a25-91b3-bba0cde7f8ce">Disconnect</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/deb8e05e-a6dc-4971-9c34-9c12f1dedc9e">DomainChange</a>
</td>
<td>Occurs when the DVD domain changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/76b1eebb-45d9-40fc-a845-24a7dac8c96c">DoubleClick</a>
</td>
<td>Occurs when the user double-clicks a mouse button.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/03041012-fbb7-42ee-84a6-80b90091fedd">DurationUnitChange</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/1f4e3a69-da55-4adf-87ab-118954070096">EndOfStream</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/65c17590-3988-40d8-b6d8-b32b2e883059">Error</a>
</td>
<td>Occurs when the Windows Media Player control has an error condition.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3759d40c-414a-4f91-93eb-0ad4a4b091b9">KeyDown</a>
</td>
<td>Occurs when a key is pressed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/72d97c04-6978-4275-9adf-2deeebb34224">KeyPress</a>
</td>
<td>Occurs when a key is pressed and then released.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e76e11d8-6cb9-488e-b5ca-1b5b11898d4b">KeyUp</a>
</td>
<td>Occurs when a key is released.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5caf2982-d562-4306-b211-58741622c94c">MarkerHit</a>
</td>
<td>Occurs when a marker is reached.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/385fb52c-62d2-482d-bc9f-94dbf693a27c">MediaChange</a>
</td>
<td>Occurs when a media item changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c18aa7d1-2788-473d-8ade-5e897b83a4d6">MediaCollectionAttributeStringAdded</a>
</td>
<td>Occurs when an attribute is added to the library.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/76767c3d-4dc1-4964-a337-6cde8f4c8609">MediaCollectionAttributeStringChanged</a>
</td>
<td>Occurs when an attribute in the library is changed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4e7a3d71-4ec1-4c33-9101-d9d90ee8b1f9">MediaCollectionAttributeStringRemoved</a>
</td>
<td>Occurs when an attribute is removed from the library.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8de74905-a0be-46a7-8653-bb955c098257">MediaCollectionChange</a>
</td>
<td>Occurs when the media collection changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3c48ff94-01d6-492c-912c-ee74b619730b">MediaError</a>
</td>
<td>Occurs when the <b>Media</b> object has an error condition.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/64761f19-914a-4ab5-aeb9-12c0aefc8113">ModeChange</a>
</td>
<td>Occurs when a mode of Windows Media Player is changed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4fbf1fdf-3d15-4d43-b319-5c83712e7f2f">MouseDown</a>
</td>
<td>Occurs when a mouse button is pressed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/ca0b438f-2093-41b0-9170-ec59656b70e1">MouseMove</a>
</td>
<td>Occurs when the mouse pointer is moved.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/314d633f-e2f4-43ff-951f-1403c1ccd571">MouseUp</a>
</td>
<td>Occurs when a mouse button is released.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/829cb422-eb24-4280-b565-de42c5a77b5f">NewStream</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/08fef94e-82ef-4606-a7d5-6258fddd8717">OpenPlaylistSwitch</a>
</td>
<td>Occurs when a title on a DVD begins playing.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6f228bc5-39a4-4bf8-a887-43ba13c1c414">OpenStateChange</a>
</td>
<td>Occurs when the Windows Media Player control changes state.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6fbe545a-2130-4cda-a663-6103d938aef4">PlayerDockedStateChange</a>
</td>
<td>Occurs when a remoted Windows Media Player control docks or undocks.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/16e9aa76-8ecf-471e-a30c-b8cf834cee0e">PlayerReconnect</a>
</td>
<td>Occurs when a remoted Windows Media Player control reconnects to the Player.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a2847bda-3003-4c80-abc1-5c873d0810b7">PlaylistChange</a>
</td>
<td>Occurs when a playlist changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/dcef72f0-3b56-466b-9431-17a7b8130292">PlaylistCollectionChange</a>
</td>
<td>Occurs when something changes in the playlist collection.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f865021c-692b-425e-a37a-b3048f7e5c64">PlaylistCollectionPlaylistAdded</a>
</td>
<td>Occurs when a playlist is added to the playlist collection.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/53b7e883-f392-4a07-8952-ab7a6e9c436e">PlaylistCollectionPlaylistRemoved</a>
</td>
<td>Occurs when a playlist is removed from the playlist collection.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c54e936f-eca8-41ca-8a2d-94e67b5a9a49">PlaylistCollectionPlaylistSetAsDeleted</a>
</td>
<td>Reserved for future use.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/d7bd4fde-8b08-4450-b291-1249393b5388">PlayStateChange</a>
</td>
<td>Occurs when the play state of the Windows Media Player control changes.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/644aaab0-8028-4dd2-9f56-f97db2b22d69">PositionChange</a>
</td>
<td>Occurs when the current position of the media has been changed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/1010961f-6d06-455a-9c14-bc06702e9e89">ScriptCommand</a>
</td>
<td>Occurs when a synchronized command or URL is received.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/0397ae20-bc8b-4b7e-8d5d-2b1fb427355a">StatusChange</a>
</td>
<td>Occurs when the <b>status</b> property changes value.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3f6d6a77-8d8a-4ed8-8222-95086c08037c">SwitchedToControl</a>
</td>
<td>Occurs when a remoted Windows Media Player control switches to the docked state.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b77a1d6a-8bfb-4548-9347-ab098a5fcfd9">SwitchedToPlayerApplication</a>
</td>
<td>Occurs when a remoted Windows Media Player control switches to the full mode of the Player.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/d68a2e17-c9db-4ad7-b7e8-ea7740de2980">Warning</a>
</td>
<td>Reserved for future use.</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/61cd0a2e-b94f-4c10-b3e2-ad1dc2a0b17d">IWMPEvents2 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

