---
UID: NN:strmif.IDvdControl2
title: IDvdControl2 (strmif.h)
description: The IDvdControl2 interface navigates and plays DVD-Video titles.helpviewer_keywords: ["IDvdControl2","IDvdControl2 interface [DirectShow]","IDvdControl2 interface [DirectShow]","described","IDvdControl2Interface","dshow.idvdcontrol2","strmif/IDvdControl2"]
old-location: dshow\idvdcontrol2.htm
tech.root: DirectShow
ms.assetid: eda43b20-1c4d-4769-bb87-3942716af13c
ms.date: 12/05/2018
ms.keywords: IDvdControl2, IDvdControl2 interface [DirectShow], IDvdControl2 interface [DirectShow],described, IDvdControl2Interface, dshow.idvdcontrol2, strmif/IDvdControl2
f1_keywords:
- strmif/IDvdControl2
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDvdControl2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2 interface


## -description



The <code>IDvdControl2</code> interface navigates and plays DVD-Video titles. The DirectShow <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> source filter implements this interface. After creating a DVD filter graph through the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdgraphbuilder">IDvdGraphBuilder</a> interface, a DVD player application uses the methods of the <b>IDvdControl2</b> and <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> interfaces to send DVD commands to and retrieve state information from the DVD Navigator.

<code>IDvdControl2</code> provides the full functionality required by the DVD Annex J specification, as well as methods for playback, menu navigation, and parental control. For more information on writing a DVD player application using the DVD Navigator, including topics on the DVD filter graph, command synchronization, parental controls, menus, and karaoke support, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>.</p>Playback


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdControl2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdControl2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-acceptparentallevelchange">AcceptParentalLevelChange</a>
</td>
<td align="left" width="63%">
Accepts or rejects a request from the DVD Navigator to play content at a higher parental management level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-activateatposition">ActivateAtPosition</a>
</td>
<td align="left" width="63%">
Activates the menu button under the mouse pointer position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-activatebutton">ActivateButton</a>
</td>
<td align="left" width="63%">
Activates the selected menu button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses or resumes playback at the current location. (Deprecated.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playattime">PlayAtTime</a>
</td>
<td align="left" width="63%">
Starts playback from the specified time in the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playattimeintitle">PlayAtTimeInTitle</a>
</td>
<td align="left" width="63%">
Starts playback from the specified time in the specified title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playbackwards">PlayBackwards</a>
</td>
<td align="left" width="63%">
Plays backward at the specified speed from the current location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playchapter">PlayChapter</a>
</td>
<td align="left" width="63%">
Starts playback from the specified chapter in the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playchapterintitle">PlayChapterInTitle</a>
</td>
<td align="left" width="63%">
Starts playback from the beginning of the specified chapter of the specified title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playchaptersautostop">PlayChaptersAutoStop</a>
</td>
<td align="left" width="63%">
Plays the number of chapters specified, starting at the specified chapter within the specified title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playforwards">PlayForwards</a>
</td>
<td align="left" width="63%">
Plays forward at the specified speed from the current location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playnextchapter">PlayNextChapter</a>
</td>
<td align="left" width="63%">
Starts playback from the beginning of the next chapter in the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop">PlayPeriodInTitleAutoStop</a>
</td>
<td align="left" width="63%">
Starts playback in the specified title from the specified start time until the specified end time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playprevchapter">PlayPrevChapter</a>
</td>
<td align="left" width="63%">
Starts playback from the beginning of the previous chapter in the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playtitle">PlayTitle</a>
</td>
<td align="left" width="63%">
Starts playback from the beginning of the specified title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-replaychapter">ReplayChapter</a>
</td>
<td align="left" width="63%">
Starts playback from the beginning of the current chapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-resume">Resume</a>
</td>
<td align="left" width="63%">
Leaves a menu and resumes playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-returnfromsubmenu">ReturnFromSubmenu</a>
</td>
<td align="left" width="63%">
Returns the display from a submenu to its parent menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectandactivatebutton">SelectAndActivateButton</a>
</td>
<td align="left" width="63%">
Selects and activates the specified menu button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectangle">SelectAngle</a>
</td>
<td align="left" width="63%">
Sets the new angle when the DVD Navigator is in an angle block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectatposition">SelectAtPosition</a>
</td>
<td align="left" width="63%">
Highlights the menu button under the mouse pointer position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectaudiostream">SelectAudioStream</a>
</td>
<td align="left" width="63%">
Selects the audio stream to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectbutton">SelectButton</a>
</td>
<td align="left" width="63%">
Selects the specified menu button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectdefaultaudiolanguage">SelectDefaultAudioLanguage</a>
</td>
<td align="left" width="63%">
Sets the default audio language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage">SelectDefaultMenuLanguage</a>
</td>
<td align="left" width="63%">
Sets the default language for all menus and menu buttons.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectdefaultsubpicturelanguage">SelectDefaultSubpictureLanguage</a>
</td>
<td align="left" width="63%">
Sets the default language for subpicture text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode">SelectKaraokeAudioPresentationMode</a>
</td>
<td align="left" width="63%">
Sends karaoke auxiliary channels to the left or right speaker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectparentalcountry">SelectParentalCountry</a>
</td>
<td align="left" width="63%">
Sets the country/region for interpreting parental access levels and setting default languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectparentallevel">SelectParentalLevel</a>
</td>
<td align="left" width="63%">
Sets the parental access level for the logged-on user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectrelativebutton">SelectRelativeButton</a>
</td>
<td align="left" width="63%">
Selects the specified relative button (upper, lower, right, left).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectsubpicturestream">SelectSubpictureStream</a>
</td>
<td align="left" width="63%">
Sets the subpicture stream to display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectvideomodepreference">SelectVideoModePreference</a>
</td>
<td align="left" width="63%">
Sets the video mode display for subsequent playback—wide screen, letterbox, or pan-scan.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setdvddirectory">SetDVDDirectory</a>
</td>
<td align="left" width="63%">
Sets the DVD drive that the DVD Navigator will read from.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setgprm">SetGPRM</a>
</td>
<td align="left" width="63%">
Sets a general parameter register value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setoption">SetOption</a>
</td>
<td align="left" width="63%">
Enables or disables a DVD Navigator internal behavioral flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setstate">SetState</a>
</td>
<td align="left" width="63%">
Saves the current disc position and state of the DVD Navigator for retrieval at a later time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setsubpicturestate">SetSubpictureState</a>
</td>
<td align="left" width="63%">
Turns the subpicture display on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-showmenu">ShowMenu</a>
</td>
<td align="left" width="63%">
Displays the specified menu, if available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-stilloff">StillOff</a>
</td>
<td align="left" width="63%">
Resumes playback, canceling still mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops playback of a title or menu by moving the DVD Navigator into the DVD Stop domain.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>
 

 

