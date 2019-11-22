---
UID: NN:strmif.IDvdInfo2
title: IDvdInfo2 (strmif.h)

description: The IDvdInfo2 interface reports attributes of a DVD disc or the current state of DVD playback and navigation.
old-location: dshow\idvdinfo2.htm
tech.root: DirectShow
ms.assetid: da30d3dc-feec-4f54-b2db-a771ce404286

ms.date: 12/05/2018
ms.keywords: IDvdInfo2, IDvdInfo2 interface [DirectShow], IDvdInfo2 interface [DirectShow],described, IDvdInfo2Interface, dshow.idvdinfo2, strmif/IDvdInfo2
ms.topic: interface
f1_keywords: 
 - "strmif/IDvdInfo2"
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
 - IDvdInfo2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo2 interface


## -description



The <code>IDvdInfo2</code> interface reports attributes of a DVD disc or the current state of DVD playback and navigation. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter implements this interface. <code>IDvdInfo2</code> is the companion interface to <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> interface. <code>IDvdInfo2</code> groups the DVD Navigator's "get" methods and <b>IDvdControl2</b> groups the "set" methods. Together they provide DVD navigation and playback functionality beyond the DVD Annex J specification.

<div class="alert"><b>Note</b>  The information provided by some of these methods can also be obtained through event notifications sent from the DVD Navigator to the application's message loop. For example, to get the current DVD domain, you can call <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentdomain">IDvdInfo2::GetCurrentDomain</a> or you can handle the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/ec-dvd-domain-change">EC_DVD_DOMAIN_CHANGE</a> event in your application's message loop and extract the new domain from the event's <i>lParam1</i> parameter.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdInfo2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvdInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getallgprms">GetAllGPRMs</a>
</td>
<td align="left" width="63%">
Retrieves the current contents of all general parameter registers (GPRMs).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getallsprms">GetAllSPRMs</a>
</td>
<td align="left" width="63%">
Retrieves the current contents of all system parameter registers (SPRMs).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getaudioattributes">GetAudioAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of the specified audio stream in the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getaudiolanguage">GetAudioLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the language of the specified audio stream within the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getbuttonatposition">GetButtonAtPosition</a>
</td>
<td align="left" width="63%">
Retrieves the button located at the specified point within the display window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getbuttonrect">GetButtonRect</a>
</td>
<td align="left" width="63%">
Retrieves the rectangle coordinates of the specified button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcmdfromevent">GetCmdFromEvent</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object from an <a href="https://docs.microsoft.com/windows/desktop/DirectShow/ec-dvd-cmd-start">EC_DVD_CMD_START</a>, <a href="https://docs.microsoft.com/windows/desktop/DirectShow/ec-dvd-cmd-end">EC_DVD_CMD_END</a>, or VFW_E_DVD_CMD_CANCELLED event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentangle">GetCurrentAngle</a>
</td>
<td align="left" width="63%">
Retrieves the number of available angles in the current angle block and the currently selected angle number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentaudio">GetCurrentAudio</a>
</td>
<td align="left" width="63%">
Retrieves the number of available audio streams and the number of the currently selected audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentbutton">GetCurrentButton</a>
</td>
<td align="left" width="63%">
Retrieves the number of available buttons and the number of the currently selected button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentdomain">GetCurrentDomain</a>
</td>
<td align="left" width="63%">
Retrieves the DVD domain in which the DVD Navigator is currently located.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentlocation">GetCurrentLocation</a>
</td>
<td align="left" width="63%">
Retrieves the current playback location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentsubpicture">GetCurrentSubpicture</a>
</td>
<td align="left" width="63%">
Retrieves the number of available subpicture streams in the current title, the currently selected subpicture stream number, and the state of the subpicture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentuops">GetCurrentUOPS</a>
</td>
<td align="left" width="63%">
Retrieves a set of flags indicating which navigation commands, if any, the content authors have explicitly disabled for the current disc location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentvideoattributes">GetCurrentVideoAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the video attributes of the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdecodercaps">GetDecoderCaps</a>
</td>
<td align="left" width="63%">
Retrieves the DVD decoder's maximum data rate for video, audio, and subpicture (in forward and reverse) as well as support for various types of audio (Dolby AC-3, MPEG-2, DTS, SDDS, LPCM).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdefaultaudiolanguage">GetDefaultAudioLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the default audio language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdefaultmenulanguage">GetDefaultMenuLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the default menu language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdefaultsubpicturelanguage">GetDefaultSubpictureLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the default subpicture language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdiscid">GetDiscID</a>
</td>
<td align="left" width="63%">
Retrieves a system-generated 64-bit "unique" identification number for the specified DVD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvddirectory">GetDVDDirectory</a>
</td>
<td align="left" width="63%">
Retrieves the root directory that is set in the DVD Navigator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo">GetDVDTextLanguageInfo</a>
</td>
<td align="left" width="63%">
Retrieves the information for the specified text string language block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages">GetDVDTextNumberOfLanguages</a>
</td>
<td align="left" width="63%">
Retrieves the number of text languages for the current DVD or disc side.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative">GetDVDTextStringAsNative</a>
</td>
<td align="left" width="63%">
Retrieves the text string for the specified language as an array of bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode">GetDVDTextStringAsUnicode</a>
</td>
<td align="left" width="63%">
Retrieves the text string for the specified language in Unicode™.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdvolumeinfo">GetDVDVolumeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the current DVD volume information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getkaraokeattributes">GetKaraokeAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the karaoke attributes of the specified audio stream in the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getmenulanguages">GetMenuLanguages</a>
</td>
<td align="left" width="63%">
Retrieves all the languages available for all menus on the disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getnumberofchapters">GetNumberOfChapters</a>
</td>
<td align="left" width="63%">
Retrieves the number of chapters in a given title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getplayerparentallevel">GetPlayerParentalLevel</a>
</td>
<td align="left" width="63%">
Retrieves the current parental level and ISO 3166 country/region code settings for the DVD Navigator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getstate">GetState</a>
</td>
<td align="left" width="63%">
Retrieves a bookmark containing the disc location and DVD Navigator state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getsubpictureattributes">GetSubpictureAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of the specified subpicture stream in the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getsubpicturelanguage">GetSubpictureLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the language of the specified subpicture stream within the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettitleattributes">GetTitleAttributes</a>
</td>
<td align="left" width="63%">
Retrieves attributes of all video, audio, and subpicture streams for the specified title and its menus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettitleparentallevels">GetTitleParentalLevels</a>
</td>
<td align="left" width="63%">
Retrieves the parental levels that are defined for a particular title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettotaltitletime">GetTotalTitleTime</a>
</td>
<td align="left" width="63%">
Retrieves the total playback time for the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getvmgattributes">GetVMGAttributes</a>
</td>
<td align="left" width="63%">
Retrieves attributes of all video, audio, and subpicture streams for the video manager menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-isaudiostreamenabled">IsAudioStreamEnabled</a>
</td>
<td align="left" width="63%">
Determines if the specified audio stream is enabled in the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-issubpicturestreamenabled">IsSubpictureStreamEnabled</a>
</td>
<td align="left" width="63%">
Determines if the specified subpicture stream is enabled in the current title.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>
 

 

