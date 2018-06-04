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

# IDvdControl2 interface


## -description



The <code>IDvdControl2</code> interface navigates and plays DVD-Video titles. The DirectShow <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> source filter implements this interface. After creating a DVD filter graph through the <a href="https://msdn.microsoft.com/2179e54a-c6e2-4837-9f89-be210bde9180">IDvdGraphBuilder</a> interface, a DVD player application uses the methods of the <b>IDvdControl2</b> and <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> interfaces to send DVD commands to and retrieve state information from the DVD Navigator.

<code>IDvdControl2</code> provides the full functionality required by the DVD Annex J specification, as well as methods for playback, menu navigation, and parental control. For more information on writing a DVD player application using the DVD Navigator, including topics on the DVD filter graph, command synchronization, parental controls, menus, and karaoke support, see <a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>.</p>Playback


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdControl2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvdControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvdControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a990544e-6600-44b1-91f2-8b88fa43ccaf">AcceptParentalLevelChange</a>
</td>
<td align="left" width="63%">
Accepts or rejects a request from the DVD Navigator to play content at a higher parental management level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff9eb02c-09c0-4b58-8e38-ec84ab1f1c42">ActivateAtPosition</a>
</td>
<td align="left" width="63%">
Activates the menu button under the mouse pointer position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20213874-ed28-4e0a-83af-044570b2c7e3">ActivateButton</a>
</td>
<td align="left" width="63%">
Activates the selected menu button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>
</td>
<td align="left" width="63%">
Pauses or resumes playback at the current location. (Deprecated.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75b66e8d-3107-48ca-a887-20cf3c0b9234">PlayAtTime</a>
</td>
<td align="left" width="63%">
Starts playback from the specified time in the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/034fa82f-38d2-4031-8d7f-dcf97aa699aa">PlayAtTimeInTitle</a>
</td>
<td align="left" width="63%">
Starts playback from the specified time in the specified title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d195956b-a4e5-493f-a804-9095e3bba4e2">PlayBackwards</a>
</td>
<td align="left" width="63%">
Plays backward at the specified speed from the current location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b624aa7e-ff88-417c-8536-4ac38e8ae1ca">PlayChapter</a>
</td>
<td align="left" width="63%">
Starts playback from the specified chapter in the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ac5072b-d397-4415-b4b9-656fd59a9269">PlayChapterInTitle</a>
</td>
<td align="left" width="63%">
Starts playback from the beginning of the specified chapter of the specified title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdf9642b-ac90-4ffc-a813-4a5b22a973dd">PlayChaptersAutoStop</a>
</td>
<td align="left" width="63%">
Plays the number of chapters specified, starting at the specified chapter within the specified title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf57e2fd-c85f-430d-a1fa-5b59f7bfb8af">PlayForwards</a>
</td>
<td align="left" width="63%">
Plays forward at the specified speed from the current location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/654841ce-6689-47cc-93fb-bd8de8f4dd3a">PlayNextChapter</a>
</td>
<td align="left" width="63%">
Starts playback from the beginning of the next chapter in the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c0d647c-a0c3-428e-8368-9204049dfea8">PlayPeriodInTitleAutoStop</a>
</td>
<td align="left" width="63%">
Starts playback in the specified title from the specified start time until the specified end time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bebfe1e1-9197-4105-9b3f-edeb6f04836c">PlayPrevChapter</a>
</td>
<td align="left" width="63%">
Starts playback from the beginning of the previous chapter in the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cdea69e-7d32-470e-846b-1b2be5ca87b1">PlayTitle</a>
</td>
<td align="left" width="63%">
Starts playback from the beginning of the specified title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea1567fc-708f-4dcd-abc2-b5bdc9f6a62c">ReplayChapter</a>
</td>
<td align="left" width="63%">
Starts playback from the beginning of the current chapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/522dcb38-8c17-46b0-b5aa-5ee380057077">Resume</a>
</td>
<td align="left" width="63%">
Leaves a menu and resumes playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef213ab6-3993-46e4-803d-3ce195256e7e">ReturnFromSubmenu</a>
</td>
<td align="left" width="63%">
Returns the display from a submenu to its parent menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e5ad753-bc35-4a98-83d8-82ffccbbe3ed">SelectAndActivateButton</a>
</td>
<td align="left" width="63%">
Selects and activates the specified menu button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4acc06bc-efc3-46eb-bb71-4eb981048b36">SelectAngle</a>
</td>
<td align="left" width="63%">
Sets the new angle when the DVD Navigator is in an angle block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6cb9cb4-0792-43f5-b53b-02a38ccf0398">SelectAtPosition</a>
</td>
<td align="left" width="63%">
Highlights the menu button under the mouse pointer position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/845d00d5-3698-4cf5-bae4-abb9529c3f88">SelectAudioStream</a>
</td>
<td align="left" width="63%">
Selects the audio stream to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2903a76-2888-4f0e-b23e-36d7488c837b">SelectButton</a>
</td>
<td align="left" width="63%">
Selects the specified menu button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f5cf846-6f14-4c17-bd01-6a8ecb46fdab">SelectDefaultAudioLanguage</a>
</td>
<td align="left" width="63%">
Sets the default audio language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f45d71e5-d125-477b-8fdf-f719a6c20101">SelectDefaultMenuLanguage</a>
</td>
<td align="left" width="63%">
Sets the default language for all menus and menu buttons.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f49698cd-cc83-4f05-991d-2b3bba77c33a">SelectDefaultSubpictureLanguage</a>
</td>
<td align="left" width="63%">
Sets the default language for subpicture text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9101fd83-1349-4cdd-b5e9-6daeb7d1e3d8">SelectKaraokeAudioPresentationMode</a>
</td>
<td align="left" width="63%">
Sends karaoke auxiliary channels to the left or right speaker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb0b3fa9-c6e5-49a4-bec7-1e4e7d07ba46">SelectParentalCountry</a>
</td>
<td align="left" width="63%">
Sets the country/region for interpreting parental access levels and setting default languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c87f8b12-0c14-4d3a-ac79-98577607d053">SelectParentalLevel</a>
</td>
<td align="left" width="63%">
Sets the parental access level for the logged-on user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2eb6243a-6f69-45d2-9b72-2dd28d02e86d">SelectRelativeButton</a>
</td>
<td align="left" width="63%">
Selects the specified relative button (upper, lower, right, left).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0553a0c4-34d3-4774-9a22-acc01c0a832a">SelectSubpictureStream</a>
</td>
<td align="left" width="63%">
Sets the subpicture stream to display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d970f48e-374f-43de-a59c-6c2e70161f55">SelectVideoModePreference</a>
</td>
<td align="left" width="63%">
Sets the video mode display for subsequent playback—wide screen, letterbox, or pan-scan.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa64a614-14cb-4ea9-a005-0e738490b6d6">SetDVDDirectory</a>
</td>
<td align="left" width="63%">
Sets the DVD drive that the DVD Navigator will read from.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/192bbf1d-a5de-4acf-b8d6-8a5f733da3a6">SetGPRM</a>
</td>
<td align="left" width="63%">
Sets a general parameter register value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3b28da8-b0cb-4d76-8184-93572e4b6d06">SetOption</a>
</td>
<td align="left" width="63%">
Enables or disables a DVD Navigator internal behavioral flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3941b469-46f3-4499-9062-81a873a36292">SetState</a>
</td>
<td align="left" width="63%">
Saves the current disc position and state of the DVD Navigator for retrieval at a later time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e654bc1-293b-436b-bc33-8a8f269e9aee">SetSubpictureState</a>
</td>
<td align="left" width="63%">
Turns the subpicture display on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7427ff6c-875b-40ce-aa96-3d32b607dc56">ShowMenu</a>
</td>
<td align="left" width="63%">
Displays the specified menu, if available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c419a3b-482a-4b1b-afea-6cbf9373c5b9">StillOff</a>
</td>
<td align="left" width="63%">
Resumes playback, canceling still mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops playback of a title or menu by moving the DVD Navigator into the DVD Stop domain.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>
 

 

