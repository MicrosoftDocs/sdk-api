---
UID: NN:strmif.IDvdInfo
title: IDvdInfo
author: windows-sdk-content
description: Note  This interface has been deprecated.
old-location: dshow\idvdinfo.htm
tech.root: DirectShow
ms.assetid: 6b0c5dfe-aa1b-4ad0-9272-f1351e494b11
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDvdInfo, IDvdInfo interface [DirectShow], IDvdInfo interface [DirectShow],described, IDvdInfoInterface, dshow.idvdinfo, strmif/IDvdInfo
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
 - IDvdInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a>.</div>
<div> </div>
The <b>IDvdInfo</b> interface enables an application to query for attributes of available DVD titles and the DVD player status. It also allows for control of a DVD player beyond Annex J in the DVD specification. Use this interface to retrieve details about a DVD-Video or about the current state of the DVD player filter graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvdInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/87d82404-cd43-4499-abc2-6c043c43bf4e">GetAllGPRMs</a>
</td>
<td align="left" width="63%">
Retrieves the current contents of all general parameter registers (GPRMs).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c96e0e7c-eee3-47ca-9350-94db895f1c6c">GetAllSPRMs</a>
</td>
<td align="left" width="63%">
Retrieves the current contents of all system parameter registers (SPRMs).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bb75657-d22e-47db-9389-99b51b16ca80">GetAudioLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the language of the specified audio stream within the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0526576-d313-4a64-a9ab-02cecb0c7a73">GetCurrentAngle</a>
</td>
<td align="left" width="63%">
Retrieves the number of available angles and the currently selected angle number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d542e995-3b98-402a-b1d9-253bede7dcff">GetCurrentAudio</a>
</td>
<td align="left" width="63%">
Retrieves the number of available audio streams and the number of the currently selected audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6cb0162-747a-468d-a28f-49621dd27df0">GetCurrentAudioAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes for the current audio stream in the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13df79ea-81c9-4060-8e11-ad7a24a7b5fa">GetCurrentButton</a>
</td>
<td align="left" width="63%">
Retrieves the number of available buttons and the currently selected button number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35f173d5-fb8f-47e2-ab32-87fdb197710a">GetCurrentDomain</a>
</td>
<td align="left" width="63%">
Retrieves the current DVD domain of the DVD player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27913630-d0c2-4bc1-9d6a-623f7aa631ec">GetCurrentLocation</a>
</td>
<td align="left" width="63%">
Retrieves the current playback location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92731904-2fb7-4dc2-b77f-1c40a002c469">GetCurrentSubpicture</a>
</td>
<td align="left" width="63%">
Retrieves the number of available subpicture streams, the currently selected subpicture stream number, and whether the subpicture display is disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9beb31e3-b3ff-4c7a-922f-9f1e9725ddde">GetCurrentSubpictureAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes for the current subpicture stream in the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6f48a32-c2bb-4924-9a05-469c7b79fc3e">GetCurrentUOPS</a>
</td>
<td align="left" width="63%">
Retrieves which <a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl</a> methods are valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7147d8f3-c038-4742-8667-2e40d7ab979a">GetCurrentVideoAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the current video attributes for the current title or menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2da53db9-5565-4bca-ba0a-90f7e07ccbb9">GetCurrentVolumeInfo</a>
</td>
<td align="left" width="63%">
Retrieves the current DVD volume information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e58fcd07-682a-4c41-9501-d55ba092a150">GetDVDTextInfo</a>
</td>
<td align="left" width="63%">
Retrieves the <b>TXTDT_MG</b> structure, which can contain text descriptions for title name, volume name, producer name, vocalist name, and so on, in various languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65d36d1c-956f-480f-adbb-1682eafc9c93">GetNumberOfChapters</a>
</td>
<td align="left" width="63%">
Retrieves the number of chapters that are defined for a given title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b4111db-fbb1-4da7-85e1-ddd3f5718225">GetPlayerParentalLevel</a>
</td>
<td align="left" width="63%">
Retrieves the current parental level and country/region code settings for the DVD player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3869da3-15c9-449e-bb0e-29dd4625a857">GetRoot</a>
</td>
<td align="left" width="63%">
Retrieves the root directory that is set in the player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f75ef36d-8556-4ca0-9f7f-6c09b86da24e">GetSubpictureLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the language of the specified subpicture stream within the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/012e3860-dfa2-45e8-ab37-2a3a4b2f7f9d">GetTitleAttributes</a>
</td>
<td align="left" width="63%">
Retrieves attributes of all video, audio, and subpicture streams for the specified title, including menus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a843346-9e24-4321-971f-07e4eed3fc72">GetTitleParentalLevels</a>
</td>
<td align="left" width="63%">
Retrieves the parental levels that are defined for a particular title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90f3a053-edc8-4e42-ae00-31d66d9e3115">GetTotalTitleTime</a>
</td>
<td align="left" width="63%">
Retrieves the total playback time for the current title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/449e7139-ed9f-46de-ac92-d1d67757799b">GetVMGAttributes</a>
</td>
<td align="left" width="63%">
Retrieves attributes of all video, audio, and subpicture streams for video manager (VMG) menus.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5b798477-9b36-4f59-b9cc-2938b5e4009f">Deprecated Interfaces</a>
 

 

