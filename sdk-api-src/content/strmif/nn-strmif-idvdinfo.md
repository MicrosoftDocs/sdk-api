---
UID: NN:strmif.IDvdInfo
title: IDvdInfo (strmif.h)
author: windows-sdk-content
description: Note  This interface has been deprecated.
old-location: dshow\idvdinfo.htm
tech.root: DirectShow
ms.assetid: 6b0c5dfe-aa1b-4ad0-9272-f1351e494b11
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvdInfo, IDvdInfo interface [DirectShow], IDvdInfo interface [DirectShow],described, IDvdInfoInterface, dshow.idvdinfo, strmif/IDvdInfo
ms.topic: interface
f1_keywords: 
 - "strmif/IDvdInfo"
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
 - IDvdInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a>.</div>
<div> </div>
The <b>IDvdInfo</b> interface enables an application to query for attributes of available DVD titles and the DVD player status. It also allows for control of a DVD player beyond Annex J in the DVD specification. Use this interface to retrieve details about a DVD-Video or about the current state of the DVD player filter graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvdInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getallgprms">GetAllGPRMs</a>
</td>
<td align="left" width="63%">
Retrieves the current contents of all general parameter registers (GPRMs).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getallsprms">GetAllSPRMs</a>
</td>
<td align="left" width="63%">
Retrieves the current contents of all system parameter registers (SPRMs).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getaudiolanguage">GetAudioLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the language of the specified audio stream within the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getcurrentangle">GetCurrentAngle</a>
</td>
<td align="left" width="63%">
Retrieves the number of available angles and the currently selected angle number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getcurrentaudio">GetCurrentAudio</a>
</td>
<td align="left" width="63%">
Retrieves the number of available audio streams and the number of the currently selected audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getcurrentaudioattributes">GetCurrentAudioAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes for the current audio stream in the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getcurrentbutton">GetCurrentButton</a>
</td>
<td align="left" width="63%">
Retrieves the number of available buttons and the currently selected button number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getcurrentdomain">GetCurrentDomain</a>
</td>
<td align="left" width="63%">
Retrieves the current DVD domain of the DVD player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getcurrentlocation">GetCurrentLocation</a>
</td>
<td align="left" width="63%">
Retrieves the current playback location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getcurrentsubpicture">GetCurrentSubpicture</a>
</td>
<td align="left" width="63%">
Retrieves the number of available subpicture streams, the currently selected subpicture stream number, and whether the subpicture display is disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getcurrentsubpictureattributes">GetCurrentSubpictureAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes for the current subpicture stream in the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getcurrentuops">GetCurrentUOPS</a>
</td>
<td align="left" width="63%">
Retrieves which <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl</a> methods are valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getcurrentvideoattributes">GetCurrentVideoAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the current video attributes for the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getcurrentvolumeinfo">GetCurrentVolumeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the current DVD volume information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getdvdtextinfo">GetDVDTextInfo</a>
</td>
<td align="left" width="63%">
Retrieves the <b>TXTDT_MG</b> structure, which can contain text descriptions for title name, volume name, producer name, vocalist name, and so on, in various languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getnumberofchapters">GetNumberOfChapters</a>
</td>
<td align="left" width="63%">
Retrieves the number of chapters that are defined for a given title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getplayerparentallevel">GetPlayerParentalLevel</a>
</td>
<td align="left" width="63%">
Retrieves the current parental level and country/region code settings for the DVD player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getroot">GetRoot</a>
</td>
<td align="left" width="63%">
Retrieves the root directory that is set in the player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getsubpicturelanguage">GetSubpictureLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the language of the specified subpicture stream within the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-gettitleattributes">GetTitleAttributes</a>
</td>
<td align="left" width="63%">
Retrieves attributes of all video, audio, and subpicture streams for the specified title, including menus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-gettitleparentallevels">GetTitleParentalLevels</a>
</td>
<td align="left" width="63%">
Retrieves the parental levels that are defined for a particular title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-gettotaltitletime">GetTotalTitleTime</a>
</td>
<td align="left" width="63%">
Retrieves the total playback time for the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo-getvmgattributes">GetVMGAttributes</a>
</td>
<td align="left" width="63%">
Retrieves attributes of all video, audio, and subpicture streams for video manager (VMG) menus.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
 

 

