---
UID: NN:strmif.IDvdControl
title: IDvdControl
author: windows-sdk-content
description: Note  This interface has been deprecated.
old-location: dshow\idvdcontrol.htm
tech.root: DirectShow
ms.assetid: a6ca0fe8-84e3-43e6-9421-29dcff056dfd
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IDvdControl, IDvdControl interface [DirectShow], IDvdControl interface [DirectShow],described, IDvdControlInterface, dshow.idvdcontrol, strmif/IDvdControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
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
 - strmif.h
api_name:
 - IDvdControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a>.</div>
<div> </div>
The <code>IDvdControl</code> interface controls the playback and search mechanisms of a DVD title that contains one or more video movies. Use this interface to control playback (set root drive, play, stop, and so forth) or use DVD-specific functionality such as menus and buttons when playing DVD-Video files.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvdControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvdControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a91f05d-1ded-4ecb-8850-5ee7faad134d">AngleChange</a>
</td>
<td align="left" width="63%">
Sets the new display angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08fca00b-e187-40db-99c0-8b978dd0f10e">AudioStreamChange</a>
</td>
<td align="left" width="63%">
Sets the current audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d2b1635-9b02-465a-a725-8b7985b651fb">BackwardScan</a>
</td>
<td align="left" width="63%">
Searches backward through the current disc at the specified speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a5ee6ed-2baa-45d6-a874-5df4e5c56841">ButtonActivate</a>
</td>
<td align="left" width="63%">
Activates the selected button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15ed6a4e-d798-49c9-bff3-c77207658d31">ButtonSelectAndActivate</a>
</td>
<td align="left" width="63%">
Selects and activates the specified button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c51524d0-5935-4e14-bcaf-4739fd0f21bb">ChapterPlay</a>
</td>
<td align="left" width="63%">
Plays the media file with the specified title index and chapter value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c599647-c894-47b9-a62d-3ffd22843f7c">ChapterPlayAutoStop</a>
</td>
<td align="left" width="63%">
Start playing at the specified chapter within the specified title and play the number of chapters specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1389df65-e269-4c2b-b276-a29da33fe515">ChapterSearch</a>
</td>
<td align="left" width="63%">
Halts playback of the current chapter and starts playback from the specified chapter value in the same media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dedeec1c-8565-491e-ab2c-4cdc17d988a9">ForwardScan</a>
</td>
<td align="left" width="63%">
Searches forward through the current disc at the specified speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a553a5f-f221-4161-95f1-cb1629abb87a">GoUp</a>
</td>
<td align="left" width="63%">
Halts playback of the current media file and starts playback of the designated previous program chain (PGC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a724af67-6aac-4307-97bc-a79e73621ce1">KaraokeAudioPresentationModeChange</a>
</td>
<td align="left" width="63%">
Sets the audio playback mode to karaoke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62c35cb1-f1e0-4852-9a59-555cf979615f">LeftButtonSelect</a>
</td>
<td align="left" width="63%">
Selects the left directional button from the displayed menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eba476a5-c949-4ce1-b296-314e36afc912">LowerButtonSelect</a>
</td>
<td align="left" width="63%">
Selects the lower directional button from the displayed menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0e27b7a-cf14-4b4c-849e-0fa7f6b1c0ed">MenuCall</a>
</td>
<td align="left" width="63%">
Displays the specified menu on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b5c660c-3d3f-4f78-8eca-3a42982eb0ae">MenuLanguageSelect</a>
</td>
<td align="left" width="63%">
Sets the displayed language for navigation menus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed84c7c8-0ae4-47f5-8a73-c975923722ab">MouseActivate</a>
</td>
<td align="left" width="63%">
Selects and activates a DVD button in response to a mouse click.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c843bf51-ae05-4045-b517-52daeda6bc07">MouseSelect</a>
</td>
<td align="left" width="63%">
Selects a DVD button in response to mouse movement.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a509f63f-a3e9-4b49-bbf0-f59051db119a">NextPGSearch</a>
</td>
<td align="left" width="63%">
Halts playback of the current program and starts playback from the next program within the program chain (PGC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc79ad9b-4044-4a33-83b4-f3033283058a">ParentalCountrySelect</a>
</td>
<td align="left" width="63%">
Sets the current country/region for controlling parental access levels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca572d89-b188-442d-884f-0cffa71c2892">ParentalLevelSelect</a>
</td>
<td align="left" width="63%">
Sets the parental access level for the current media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ec442dd-74ca-4b0b-901f-8efb7e77c5bf">PauseOff</a>
</td>
<td align="left" width="63%">
Unpauses the current media file playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d67a7a16-41f9-4718-a6ad-d48ba77fb1d4">PauseOn</a>
</td>
<td align="left" width="63%">
Pauses the current media file playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e2d0531-23be-471b-8094-d21771209c79">PrevPGSearch</a>
</td>
<td align="left" width="63%">
Halts playback of the current program and starts playback from the previous program within the program chain (PGC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/336908bb-369e-449d-a94a-dd22fa72f20a">Resume</a>
</td>
<td align="left" width="63%">
Returns to playing back a title from a menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67ca86cd-37a7-48ce-80d9-585d345e83fc">RightButtonSelect</a>
</td>
<td align="left" width="63%">
Selects the right directional button from the displayed menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3068edc0-c052-4f44-9f62-453320af20a3">SetRoot</a>
</td>
<td align="left" width="63%">
Sets the root directory containing the DVD-Video volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f466728-027e-40d6-b8f8-ed0aad02dd1e">StillOff</a>
</td>
<td align="left" width="63%">
Resumes playback, canceling still mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61c5b863-038b-4c4a-a7a4-d1fd1801f843">StopForResume</a>
</td>
<td align="left" width="63%">
Transitions playback to the DVD_DOMAIN_Stop state after saving resume information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/527031fa-bab9-49f5-89b1-f0c5c5812a76">SubpictureStreamChange</a>
</td>
<td align="left" width="63%">
Selects the new subpicture stream and enables or disables it for display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56b4b086-e315-486c-8dbd-97960f5b76d1">TimePlay</a>
</td>
<td align="left" width="63%">
Plays the media file with the specified title index, starting at the specified time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2e6848e-569e-44f0-b676-e22e4df07d8d">TimeSearch</a>
</td>
<td align="left" width="63%">
Halts playback of the current chapter and starts playback from the specified time in the same media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ca710f0-8f08-43d6-8cc1-a25068d5e0ef">TitlePlay</a>
</td>
<td align="left" width="63%">
Finds the media file with the specified title index and plays it back.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35a621de-5110-4999-8475-ae84a4dc9ee1">TopPGSearch</a>
</td>
<td align="left" width="63%">
Halts playback of the current program and restarts playback of the current program within the program chain (PGC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd0e4086-087b-460f-a6af-fa073644f1bb">UpperButtonSelect</a>
</td>
<td align="left" width="63%">
Selects the upper directional button from the displayed menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e68b09c-534c-46d2-bda0-72f3d1d86b66">VideoModePreferrence</a>
</td>
<td align="left" width="63%">
Sets the video display mode the user prefers.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5b798477-9b36-4f59-b9cc-2938b5e4009f">Deprecated Interfaces</a>
 

 

