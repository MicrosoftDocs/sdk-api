---
UID: NN:strmif.IDvdInfo2
title: IDvdInfo2
author: windows-sdk-content
description: The IDvdInfo2 interface reports attributes of a DVD disc or the current state of DVD playback and navigation.
old-location: dshow\idvdinfo2.htm
tech.root: DirectShow
ms.assetid: da30d3dc-feec-4f54-b2db-a771ce404286
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IDvdInfo2, IDvdInfo2 interface [DirectShow], IDvdInfo2 interface [DirectShow],described, IDvdInfo2Interface, dshow.idvdinfo2, strmif/IDvdInfo2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo2 interface


## -description



The <code>IDvdInfo2</code> interface reports attributes of a DVD disc or the current state of DVD playback and navigation. The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter implements this interface. <code>IDvdInfo2</code> is the companion interface to <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> interface. <code>IDvdInfo2</code> groups the DVD Navigator's "get" methods and <b>IDvdControl2</b> groups the "set" methods. Together they provide DVD navigation and playback functionality beyond the DVD Annex J specification.

<div class="alert"><b>Note</b>  The information provided by some of these methods can also be obtained through event notifications sent from the DVD Navigator to the application's message loop. For example, to get the current DVD domain, you can call <a href="https://msdn.microsoft.com/ad850402-7b48-4517-a55f-42cfa75d3ee6">IDvdInfo2::GetCurrentDomain</a> or you can handle the <a href="https://msdn.microsoft.com/4faa46d6-2ba2-44a3-b237-acac3b32f8b1">EC_DVD_DOMAIN_CHANGE</a> event in your application's message loop and extract the new domain from the event's <i>lParam1</i> parameter.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdInfo2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvdInfo2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/994f57b5-8514-4768-a679-21133ec92e32">GetAllGPRMs</a>
</td>
<td align="left" width="63%">
Retrieves the current contents of all general parameter registers (GPRMs).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a5fb447-670d-4f1f-838e-266843185efe">GetAllSPRMs</a>
</td>
<td align="left" width="63%">
Retrieves the current contents of all system parameter registers (SPRMs).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80291efa-f3eb-47f0-94e0-dcde583ff35c">GetAudioAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of the specified audio stream in the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c95afa36-879b-4fd5-bf92-0b9b93c708ef">GetAudioLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the language of the specified audio stream within the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9c506b3-c9d9-4dc2-b318-f987ab8636dc">GetButtonAtPosition</a>
</td>
<td align="left" width="63%">
Retrieves the button located at the specified point within the display window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8825979c-2a98-462a-acf9-939c81ece89a">GetButtonRect</a>
</td>
<td align="left" width="63%">
Retrieves the rectangle coordinates of the specified button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/488a394f-222f-4536-a20a-579df5c2f91f">GetCmdFromEvent</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/85f9b208-ddc2-4d9c-a30b-b666c81a49d2">IDvdCmd</a> object from an <a href="https://msdn.microsoft.com/230116b4-23f1-4c37-a781-da2c5aa20a1f">EC_DVD_CMD_START</a>, <a href="https://msdn.microsoft.com/f460db8e-b966-41fa-bfa1-4ad3fa65c3e3">EC_DVD_CMD_END</a>, or VFW_E_DVD_CMD_CANCELLED event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9347cad1-f061-45e9-ab4a-66e87a2b0c86">GetCurrentAngle</a>
</td>
<td align="left" width="63%">
Retrieves the number of available angles in the current angle block and the currently selected angle number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f2ff79f-cefa-43e5-ab91-348a5341a171">GetCurrentAudio</a>
</td>
<td align="left" width="63%">
Retrieves the number of available audio streams and the number of the currently selected audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e8d8a0e-6db8-495b-b968-8a4e63435b99">GetCurrentButton</a>
</td>
<td align="left" width="63%">
Retrieves the number of available buttons and the number of the currently selected button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad850402-7b48-4517-a55f-42cfa75d3ee6">GetCurrentDomain</a>
</td>
<td align="left" width="63%">
Retrieves the DVD domain in which the DVD Navigator is currently located.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54005c07-1689-411c-88a9-bcd19cc065dd">GetCurrentLocation</a>
</td>
<td align="left" width="63%">
Retrieves the current playback location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d41fb9ad-83e3-46d6-90b3-abdc61a6b997">GetCurrentSubpicture</a>
</td>
<td align="left" width="63%">
Retrieves the number of available subpicture streams in the current title, the currently selected subpicture stream number, and the state of the subpicture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71ae88f0-17ad-4530-b2e7-6a8155c14a97">GetCurrentUOPS</a>
</td>
<td align="left" width="63%">
Retrieves a set of flags indicating which navigation commands, if any, the content authors have explicitly disabled for the current disc location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92bd3af9-7057-4bf7-9026-d4862c271a03">GetCurrentVideoAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the video attributes of the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfaf475c-336a-492f-b5a8-c49c21e5392d">GetDecoderCaps</a>
</td>
<td align="left" width="63%">
Retrieves the DVD decoder's maximum data rate for video, audio, and subpicture (in forward and reverse) as well as support for various types of audio (Dolby AC-3, MPEG-2, DTS, SDDS, LPCM).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89f93521-9df7-4162-bb66-2210cceebc75">GetDefaultAudioLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the default audio language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2ad5bec-fc8c-4fcf-8657-aa1726c28cdc">GetDefaultMenuLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the default menu language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ada423a5-90ef-48e1-80fa-04d0a24da8f7">GetDefaultSubpictureLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the default subpicture language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53c244ff-026f-4838-b805-316ef3d872d1">GetDiscID</a>
</td>
<td align="left" width="63%">
Retrieves a system-generated 64-bit "unique" identification number for the specified DVD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fad4dd0a-4831-4460-9631-ed06b6647f2d">GetDVDDirectory</a>
</td>
<td align="left" width="63%">
Retrieves the root directory that is set in the DVD Navigator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af8662af-f306-4142-b563-3b40a98b7fbe">GetDVDTextLanguageInfo</a>
</td>
<td align="left" width="63%">
Retrieves the information for the specified text string language block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20c6ee1f-f20b-40c5-bc84-5ec1c07c0681">GetDVDTextNumberOfLanguages</a>
</td>
<td align="left" width="63%">
Retrieves the number of text languages for the current DVD or disc side.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a162b4ad-28f2-49fc-9b32-72538be9ddd5">GetDVDTextStringAsNative</a>
</td>
<td align="left" width="63%">
Retrieves the text string for the specified language as an array of bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e13d4212-0e4a-40cf-89c7-f0c22f5a5cb9">GetDVDTextStringAsUnicode</a>
</td>
<td align="left" width="63%">
Retrieves the text string for the specified language in Unicode™.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d55973af-5f56-4e22-b3b0-2cee9f57c2d4">GetDVDVolumeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the current DVD volume information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c69ea1e0-8d8a-4cd3-86a4-a2d481160a2e">GetKaraokeAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the karaoke attributes of the specified audio stream in the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97c95208-e2fc-4c9a-b8ba-61419b96aec9">GetMenuLanguages</a>
</td>
<td align="left" width="63%">
Retrieves all the languages available for all menus on the disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5899fa87-56e2-4287-9325-1d9eaedb892b">GetNumberOfChapters</a>
</td>
<td align="left" width="63%">
Retrieves the number of chapters in a given title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ae9b79a-1a2e-4679-9ead-6892491a1af3">GetPlayerParentalLevel</a>
</td>
<td align="left" width="63%">
Retrieves the current parental level and ISO 3166 country/region code settings for the DVD Navigator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/403add2b-3dfd-436d-8184-7a14f30f6ea3">GetState</a>
</td>
<td align="left" width="63%">
Retrieves a bookmark containing the disc location and DVD Navigator state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3dce0c01-1d39-4f49-984b-8cce08a2e67b">GetSubpictureAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of the specified subpicture stream in the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/175ab238-59a9-4142-921b-ed374423f4e3">GetSubpictureLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the language of the specified subpicture stream within the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e901e14-9e98-4ca5-ae37-7a4564b187ab">GetTitleAttributes</a>
</td>
<td align="left" width="63%">
Retrieves attributes of all video, audio, and subpicture streams for the specified title and its menus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00c9d1e5-1b1f-41b3-b06c-0b78e2d2db0b">GetTitleParentalLevels</a>
</td>
<td align="left" width="63%">
Retrieves the parental levels that are defined for a particular title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90768da1-592a-49ec-99b0-56f463c322e8">GetTotalTitleTime</a>
</td>
<td align="left" width="63%">
Retrieves the total playback time for the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddb1059a-e1c5-4506-b565-fd871ad8385f">GetVMGAttributes</a>
</td>
<td align="left" width="63%">
Retrieves attributes of all video, audio, and subpicture streams for the video manager menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34938f9b-d3d8-4f38-95b4-bd65a5e88458">IsAudioStreamEnabled</a>
</td>
<td align="left" width="63%">
Determines if the specified audio stream is enabled in the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19facb38-8bc4-4605-9b2b-2a123b67aeb6">IsSubpictureStreamEnabled</a>
</td>
<td align="left" width="63%">
Determines if the specified subpicture stream is enabled in the current title.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>
 

 

