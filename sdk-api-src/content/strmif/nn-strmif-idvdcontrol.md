---
UID: NN:strmif.IDvdControl
title: IDvdControl (strmif.h)
description: Note  This interface has been deprecated.
helpviewer_keywords: ["IDvdControl","IDvdControl interface [DirectShow]","IDvdControl interface [DirectShow]","described","IDvdControlInterface","dshow.idvdcontrol","strmif/IDvdControl"]
old-location: dshow\idvdcontrol.htm
tech.root: DirectShow
ms.assetid: a6ca0fe8-84e3-43e6-9421-29dcff056dfd
ms.date: 12/05/2018
ms.keywords: IDvdControl, IDvdControl interface [DirectShow], IDvdControl interface [DirectShow],described, IDvdControlInterface, dshow.idvdcontrol, strmif/IDvdControl
f1_keywords:
- strmif/IDvdControl
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a>.</div>
<div> </div>
The <code>IDvdControl</code> interface controls the playback and search mechanisms of a DVD title that contains one or more video movies. Use this interface to control playback (set root drive, play, stop, and so forth) or use DVD-specific functionality such as menus and buttons when playing DVD-Video files.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-anglechange">AngleChange</a>
</td>
<td align="left" width="63%">
Sets the new display angle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-audiostreamchange">AudioStreamChange</a>
</td>
<td align="left" width="63%">
Sets the current audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-backwardscan">BackwardScan</a>
</td>
<td align="left" width="63%">
Searches backward through the current disc at the specified speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-buttonactivate">ButtonActivate</a>
</td>
<td align="left" width="63%">
Activates the selected button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-buttonselectandactivate">ButtonSelectAndActivate</a>
</td>
<td align="left" width="63%">
Selects and activates the specified button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-chapterplay">ChapterPlay</a>
</td>
<td align="left" width="63%">
Plays the media file with the specified title index and chapter value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-chapterplayautostop">ChapterPlayAutoStop</a>
</td>
<td align="left" width="63%">
Start playing at the specified chapter within the specified title and play the number of chapters specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-chaptersearch">ChapterSearch</a>
</td>
<td align="left" width="63%">
Halts playback of the current chapter and starts playback from the specified chapter value in the same media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-forwardscan">ForwardScan</a>
</td>
<td align="left" width="63%">
Searches forward through the current disc at the specified speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-goup">GoUp</a>
</td>
<td align="left" width="63%">
Halts playback of the current media file and starts playback of the designated previous program chain (PGC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-karaokeaudiopresentationmodechange">KaraokeAudioPresentationModeChange</a>
</td>
<td align="left" width="63%">
Sets the audio playback mode to karaoke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-leftbuttonselect">LeftButtonSelect</a>
</td>
<td align="left" width="63%">
Selects the left directional button from the displayed menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-lowerbuttonselect">LowerButtonSelect</a>
</td>
<td align="left" width="63%">
Selects the lower directional button from the displayed menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-menucall">MenuCall</a>
</td>
<td align="left" width="63%">
Displays the specified menu on the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-menulanguageselect">MenuLanguageSelect</a>
</td>
<td align="left" width="63%">
Sets the displayed language for navigation menus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-mouseactivate">MouseActivate</a>
</td>
<td align="left" width="63%">
Selects and activates a DVD button in response to a mouse click.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-mouseselect">MouseSelect</a>
</td>
<td align="left" width="63%">
Selects a DVD button in response to mouse movement.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-nextpgsearch">NextPGSearch</a>
</td>
<td align="left" width="63%">
Halts playback of the current program and starts playback from the next program within the program chain (PGC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-parentalcountryselect">ParentalCountrySelect</a>
</td>
<td align="left" width="63%">
Sets the current country/region for controlling parental access levels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-parentallevelselect">ParentalLevelSelect</a>
</td>
<td align="left" width="63%">
Sets the parental access level for the current media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-pauseoff">PauseOff</a>
</td>
<td align="left" width="63%">
Unpauses the current media file playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-pauseon">PauseOn</a>
</td>
<td align="left" width="63%">
Pauses the current media file playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-prevpgsearch">PrevPGSearch</a>
</td>
<td align="left" width="63%">
Halts playback of the current program and starts playback from the previous program within the program chain (PGC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-resume">Resume</a>
</td>
<td align="left" width="63%">
Returns to playing back a title from a menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-rightbuttonselect">RightButtonSelect</a>
</td>
<td align="left" width="63%">
Selects the right directional button from the displayed menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-setroot">SetRoot</a>
</td>
<td align="left" width="63%">
Sets the root directory containing the DVD-Video volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-stilloff">StillOff</a>
</td>
<td align="left" width="63%">
Resumes playback, canceling still mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-stopforresume">StopForResume</a>
</td>
<td align="left" width="63%">
Transitions playback to the DVD_DOMAIN_Stop state after saving resume information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-subpicturestreamchange">SubpictureStreamChange</a>
</td>
<td align="left" width="63%">
Selects the new subpicture stream and enables or disables it for display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-timeplay">TimePlay</a>
</td>
<td align="left" width="63%">
Plays the media file with the specified title index, starting at the specified time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-timesearch">TimeSearch</a>
</td>
<td align="left" width="63%">
Halts playback of the current chapter and starts playback from the specified time in the same media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-titleplay">TitlePlay</a>
</td>
<td align="left" width="63%">
Finds the media file with the specified title index and plays it back.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-toppgsearch">TopPGSearch</a>
</td>
<td align="left" width="63%">
Halts playback of the current program and restarts playback of the current program within the program chain (PGC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-upperbuttonselect">UpperButtonSelect</a>
</td>
<td align="left" width="63%">
Selects the upper directional button from the displayed menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-videomodepreferrence">VideoModePreferrence</a>
</td>
<td align="left" width="63%">
Sets the video display mode the user prefers.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
 

 

